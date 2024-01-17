النهاردة هنتكلم عن طريقة استرجاع بيانات من ال SharePoint وتحويلها الي جدول واستخدام الجدول سواء في اننا نبعته ك Email لأفراد كنوع من ال Reporting وهنتكلم في ال Section الجي عن طريقة تحويل البيانات ديه الي PDF File وتحميلها علي ال Machine الخاصة بينا
الصورة ديه فيها الشكل النهائي لل Data الي موجودة عندنا في ال Data Source بعد ما عملنا ال automation وعملنا استرجاع لل Data وخليناها تتبعت بالايميل .واحنا استخدمنا في ال Approach دا ال SharePoint List ك Data Source 
<img src="https://github.com/Kareem-Sameh/Power-Automate/assets/38144806/9b524993-b44d-49ae-8150-46aa5485bc08" width="90%"></img>


دا شكل ال SharePoint List الي استخدمناها والي فيها بيانات المستخدمين وذي ما واضح في ال Structure بتاعي انا عندي اسم المستخدم وال Action الي خده علي ال "Document" كمثال و ايضاً ال ID او الرقم التعريفي لل Action

<img src="https://github.com/Kareem-Sameh/Power-Automate/assets/38144806/bde42f9b-0c31-463c-b821-03a11e644fa8" width="90%"></img>


اول خطوة علشان نعمل شكل للايميل الي هنبعته هندخل علي https://html-online.com و هنعمل تصميم من ال window علي الشمال كأني بالظبط بعمل Word File  والموقع هيحول الكود الي انا كتبته automatically ل HTML Code 
هنا انا عملت عنوان و شكل بالنجوم و Table Header ليه background وعملت Save لل HTML Code لأننا هنستخدمه بعدين.

<img src="https://github.com/Kareem-Sameh/Power-Automate/assets/38144806/5736f2dc-7432-4160-8f36-3fe73115496c" width="90%"></img>


ثاني خطوة هعمل Table عشان استخدمه ك Table Spanner جوا ال PowerAutomate بحيث انه كل البيانات الي موجودة عندي في ال Data Source تظهر امامي علي شكل جدول.

<img src="https://github.com/Kareem-Sameh/Power-Automate/assets/38144806/49b064fd-4ffe-4f77-a5a2-ac8dccd547db" width="90%"></img>


تالت خطوة اني هعمل Create ل New Power Automate Flow وهعمل String Variable عشان يجمع كل ال Spanned Table items
رابعاً هعمل Action Get items وهخليه يجيب كل ال Data الي ليها علاقة ب Approval ID رقم 1 

<img src="https://github.com/Kareem-Sameh/Power-Automate/assets/38144806/27d9038a-dc50-4c18-9b1d-46280618174b" width="90%"></img>

خامس خطوة هعمل Action Apply to each كل item value موجودة من ال Action Get items وهعمل Append to string Variable بال HTML Code الي صممته من الموقع 
لكن هاخد بالي ان ال Value بدأت ب <tbody!--> وانتهت ب <tbody!--> وفي النص بيانات ال Item الي جت من ال apply to each عشان اخلي كل الجداول تبقا تحت بعض. فكدا يكون عندي في الاخر جدول كبير فيه كل ال Items ال Retrieved من Get items

<img src="https://github.com/Kareem-Sameh/Power-Automate/assets/38144806/801b3dab-d204-4d4e-94f3-8621c403a97b" width="90%"></img>


سادس خطوة هحط ال HTML Code الي صممتع من الموقع جوا Action Compose وبين ال <Table!-->  بتاعي هحط ال Variable Table Spanner الموجود فيه كل ال Items الي اتعملهم Append تحت بعض.

<img src="https://github.com/Kareem-Sameh/Power-Automate/assets/38144806/e2be284c-1073-49a2-8834-1b9845308108" width="90%"></img>

واخيراً استخدم ال Send Email V2 Action عشان ابعت في ال Body ال Compose Value وبكدا ال Email هيتبعت ك HTML فيه البيانات من ال SharePoint علي شكل جدول. 

<img src="https://github.com/Kareem-Sameh/Power-Automate/assets/38144806/4127819d-91eb-41cd-a7c1-f600f0c0c2e1" width="90%"></img>

تفتكر لو عاوزين نبعت ال HTML Content ديه ك PDF في ال Email as am attachement هنعمل ايه ؟ 
النقاش مفتوح.

شكراً لوقتك اتمني يكون ال Article مفيد 
شكر خاص لمن نصحني بتعريب الشرح.


