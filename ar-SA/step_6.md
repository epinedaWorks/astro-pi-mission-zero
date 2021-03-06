## قياس مقدار الرطوبة

يمكن لمستشعر الرطوبة في Astro Pi قياس الرطوبة في الهواء المحيط، وهي ميزة مفيدة تساعدتك في جمع البيانات عن الظروف في الفضاء.

![رسالة عن الرطوبة](images/degrees-message.gif)

يقيس نظام Astro Pi الرطوبة في محطة الفضاء الدولية من حيث النسبة المئوية لتركيز الماء في الهواء.

ويتمثل جزء من مهمتك في دعم طاقم محطة الفضاء الدولية فيما يتعلق بأنشطة حياتهم اليومية، إذ إن قيامك بإبلاغهم بأن مقدار الرطوبة على متن محطة الفضاء في النطاق الطبيعي أمر من شأنه أن يبعث الطمأنينة في نفوسهم.

[[[generic-theory-what-is-humidity]]]

--- task ---

أضف هذه التعليمة البرمجية لقراءة الرطوبة:

```python
humid = sense.humidity
```

سيقيس هذا السطر الرطوبة الحالية، ويخزن القيمة المقاسة في المتغير `humid`.

--- /task ---

--- task ---

وتسجل الرطوبة بدقة شديدة، أي أن القيمة المخزونة سيكون لها عدد كبير من مراتب الكسور العشرية. يمكنك تقريب القيمة إلى أي عدد من الخانات الكسرية. في هذا المثال قمنا بالتقريب إلى خانة كسرية واحدة، ولكن للحصول على مستوى مختلف من الدقة، غيِّر العدد`1` إلى عدد الخانات الكسرية التي تريد مشاهدتها.

```python
humid = round( sense.humidity, 1 )
```

--- /task ---

--- task ---

لعرض الرطوبة الحالية كرسالة تمرر على الشاشة، أضف هذا السطر من التعليمة البرمجية:

```python
sense.show_message( str(temp) )
```

الجزء `str()` يحوِّل الرطوبة من عدد إلى نص حتى يتمكن Astro Pi من عرضه.

--- /task ---

--- task ---

يمكنك أيضا عرض الرطوبة كجزء من رسالة أخرى عن طريق ربط أجزاء رسالتك بواسطة `+`.

```python
sense.show_message( "It is " + str(temp) + " degrees" )
```

--- /task ---

Astro Pi الحقيقي سوف يقيس الرطوبة حوله، ولكن يمكنك تحريك شريط تمرير الرطوبة على محاكي Sense HAT لمحاكاة تغييرات الرطوبة واختبار التعليمة البرمجية الخاص بك.

![منزلق الرطوبة](images/humidity-slider.png)

**ملاحظة:** قد تتساءل لماذا يظهر شريط تمرير الرطوبة كرقم صحيح، ولكن القراءة التي تحصل عليها هي كسر عشري. يحاكي المحاكي عدم الدقة الطفيفة للاستشعار الحقيقي، لذا فإن قياس الرطوبة الذي تراه قد يكون أكبر أو أصغر قليلا من القيمة التي قمت بتعيينها مع شريط التمرير.