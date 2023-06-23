# تعلم كيف تقوم بتحويل حاسوبك الشخصي الى جهاز آمن للاستخدام وحتى معزول تماما عن الانترنت Air-gap بشكل مؤقت باستخدام نظام تشغيل Tails عالي الامن

::: tip طجلأ - طويلة جدا لن أقرأها
نظام تشغيل Tails هو نظام حاسوب شبيه بنظام الويندوز ولكنه مجاني، مفتوح المصدر ومخصص للعمل على الحاسوب بشكل أمن جدا وبخصوصية تامة بشكل مؤقت من ذاكرة الفلاشة. عندما إنتهاء العمل عليه وبمجرد إغلاقة تختفي كل المعلومات منه ويعود الحاسوب الى حالته السابقة وكأن شيئا لم يحدث. 
:::

نظام تشغيل تييلز هو اختصار للكلمات التالية `The Amnesic Incognito Live System - Tails` واقرب معنى له بالعربية هو نظام تشغيل مؤقت مستخفي وفاقد للذاكرة.

يعمل [نظام Tails](https://tails.boum.org) كنظام مستقل تماما عن نظام التشغيل الافتراضي المثبت على جهاز الحاسوب (كالويندوز)،  يتم تنصيبه على قطعة فلاشة USB Flash Drive بحيث عندما تدخلها الى اي حاسوب يتم تشغيل نظام Tails منها بمساعدة ذاكرة الحاسوب المؤقتة (ذاكرة الوصول العشوائي RAM - Random Access Memory أو ما تعرف بذاكرة القراءة والكتابة) إذ أن المعلومات تُفقد منها بمجرد انقطاع التيار عنها. 

لذلك هو نظام تشغيل مؤقت (LiveOS -Live Operation System) الذي بدورة يقوم باستخدام موارد الحاسوب (الهاردويز) كوحدة المعلاجة، كرت الشاشة، لوحةالمفاتيح، الشاشة، وغيرها، ما عدا القرص الصلب لكي يتجنب تشغيل النظام الافتراضي الحالي(كالويندوز) ولكي لا يترك اي أثر على الحاسوب.

![Tails](/images/tails-os/laptop.svg)

## 🔘مميزات نظام تشغيل Tails
يتميز نظام تشغيل Tails عن باقي أنظمة التشغيل العادية بعدة مميزات منها:
- يعمل نظام Tails من قطعة فلاشة USB Flash Drive عند ادخالة الى أي حاسوب تلقائياً عقب الإقلاع.
 - يختفي كل ما فعلته على جهاز الحاسوب بمجرد إغلاق Tails أو بمجرد فصل الفلاشة من الحاسوب ليعود لوضعه الطبيعي بعد ذلك بنظام تشغيله الافتراضي كالويندوز. 
 - لا يترك اي معلومات على القرص الصلب في الحاسوب كما وانه لا يترك اي معلومات على الفلاشة (بوضعه الافتراضي) أي ان عند تشغيله مجددا يبدأ النظام من جديد كُليا كما لو كانت هذة اول مرة تقوم باستخدامه
- بضغطة زر يمكن وضع الجهاز بحالة الطيران ليتم فصله عن الانترنت من خلال عدم تفعيل كرت الانترنت يشمل كرت الوافي - Wifi. كما ان كرت البلوتوث Bluetooth وكرت ال GPS لا يتم تشغيلهم بتاتا.
- عند توصيله بالانترنت يتم تحويل جميع الاتصالات عبر شبكة تور Tor فقط ولا يمكن الاتصال مباشرة بالانترنت الا عبر [شبكة تور](tor-browser)
- يحتوي على مجموعة كبيرة من البرامج والتطبيقات المجانية ومفتوحة المصدر والتي تمكنكم من العمل عليه فورا دون الحاجة لتنصيب اي برامج إضافية اخرى، برامج مثل أوفيس LibreOffice، محفظة بيتكوين Electrum Wallet وغيرها.
- يمكن العمل على أي حاسوب حتى لو كان الحاسوب مليئ بالفيروسات وبرامج التعقب لانه ببساطة لا يُفعل نظام التشغيل الافتراضي اصلا ويقوم بتجاهل القرص الصلب تماما. حتى انه بامكانك ازالة القرص الصلب ومع ذلك سيعمل نظام Tails من قطعة الفلاشة.
- اذا اردت يمكن تعديل النظام ليسمح بتخزين دائم لبعض الملفات على قطعة الفلاشة USB Flash Drive بشكل مشفر.

::: danger لنفرض انك تعمل على حاسوب بنظام الويندوز لكي تشغل نظام Tails كل ما عليك فعله هو:
1. تطفئ الحاسوب
2. توصل الفلاشة بالحاسوب عبر ال USB  (المنصب عليها Tails )
3. تشغل الحاسوب فيشتغل نظام Tails
4. تعمل ما تريد ان تفعله على النظام
5. تطفى الحاسوب وتخرج الفلاشة
6. اختفى كل شيى من الحاسوب والفلاشة عادت بنظام Tails جديد
::: 

## 🔘كيف يمكن لنظام Tails ان يكون أداة مهمة من أدوات بتكوين
نظام تشغيل كهذا تستطيع عزله عن الانترنت بسهولة، لا يحتفظ بأي شيئ عليه ولا يترك اي اثر على الجهاز الذي تستعمله عند انتهاء العمل عليه، هو بالضبط الميزة التي قامت عليها [محفظة SeedSigner](seedsigner)  هذة الميزة تسمى (Statless). لذلك نستطيع استعمال هذا النظام لتوقيع عمليات بيتكوين بشكل امن بنسبة عالية جدا.  

هذة الطريقة قد لا تكون الطريقة الافضل والاسهل للتعامل مع البيتكوين ولكن لكل شخص ظروفه. 
- قد تكون موجود في دولة او مكان بالعالم لا يمكنك شراء جهاز توقيع [محفظة باردة صلبة ](/wallets) كبلد محظور اقتصاديا.
- قد تكون في بلد ممنوع به امتلاك البيتكوين اصلا ومجرد شرائك لجهاز كهذا قد يسبب لك المتاعب مع السلطات عند وصول الطرد اليك من الخارج. 
- أو انك لا تثق بان الطرد قد يصل اليك مباشرة من الشركة المصنعة له من دون ان يمسسه احد ويقوم بتعديله [إقرا عن حادثة supply chain attack](https://www.kaspersky.com/blog/fake-trezor-hardware-crypto-wallet/48155/)
- أو انك لا تثق بالمرة بالشركات المصنعة لأجهزة التوقيع (المحافظ الباردة).
- أو انك لا تريد ان يكون اسمك وتفاصيلك الشخصية في قائمة الزبائن للشركة المصنعة للمحفظة التي تريد شرائها لكي لا يحدث لك كما حدث مع زبائن شركة ليدجر التي تم [اختراق قائمة بيانات زبائنها ونشرها في الانترنت](https://www.ledger.com/message-ledgers-ceo-data-leak) التي ما زالوا حتى اليوم يتعرضون لمحاولات تصيد ليتم سرقتهم.

مهما كانت ظروفك امل ان يساعدك هذا الدليل بالتعرف على الامكانيات التي يتيحها لك نظام Tails واترك لك الخيار والمسؤولية للتصرف ببيتكويناتك كما يحلو لك. فالهدف الرئيسي من هذا الموقع هو التعرف على الادوات المتاحة لك لجعل البيتكوين الخاص بك اكثر امانا واكثر مقاومة للرقابة (censorship resistance) واقل قابلية للمُصادرة والاستياء (less seizable) وليس العكس. 

لذلك نصيحتي اليك هي ان تتحلى بسلاح العلم وان تتعرف على الامكانيات المختلفة التي تتيحها لك "أدوات بيتكوين" المختلفة ولا تُقبل على فعل أي شيئ انت لم تفهمه جيدا بعد.
 
## 🔘ماذا يمكنك ان تفعله بنظام Tails كشخص مهتم بالبيتكوين
هنالك برامج منصبة وجاهز للاستعمال فورا عند تشغيل النظام منها محفظة بيتكوين تسمى [محفظة إلكتروم](verify-files-with-gpg.html#التحقق-عبر-gpg-في-نظام-windows) 

#### بما ان كل الاتصالات تمر عبر شبكة تور حتى التطبيقات والبرامج في هذا النظام فبمكانك كبتكوينر ان تستغل هذة الميزة لعدة امور:
- تصفح الانترنت من خلال [شبكة ومتصفح تور](tor-browser) المنصب وجاهز للاستعمال فورا، اذا كنت ترغب ان لا احد يعرف انك تتعامل بالبيتكوين وتتابع اخبار البيتكوين مثلا. 

- بامكانك ايضا فحص رصيد عنوان بيتكوين خاص بك عبر الدخول لموقع <https://mempool.space> دون ان تكون للموقع امكانية لمعرفة عنوان الايبي الاصلي الخاص بك
	- حتى ان الموقع لديه عنوان onion للشبكة يمكنك الدخول اليه دون الحاجة للخروج من شبكة Tor والمرور ب Exit Node بهذا العنوان:
```
http://mempoolhqx4isw62xs7abwphsq7ldayuidyx2v2oethdhhj6mlo2r6ad.onion
```	
- اذا لم يكن لديك بعد [عقدة بيتكوين كاملة](/full-node)،  يمكنك تعيين محفظة إلكتروم كمحفظة مشاهدة فقط لمراقبة حساب محفظتك بخصوصية أفضل من استعمالك للمحفظة عبر نظام الويندوز او من خلال هاتفك الذكي باتصال مباشر  بالانترنت العادي مع عقدة عشوائية، لان العقدة التي ستتصل بها محفظتك لن تعرف هويتك بفضل نظام Tails

- استعمال محفظة بيتكون كمحفظة ساخنة داخل Tails لتوقيع تحويلات بيتكوين ايضا سيكون أفضل وأمن بكثير من استعمال حاسوبك بنظام الويندوز.

#### يمكن استغلال خاصية عدم حفظ المعلومات وخاصية عزله عن الانترنت لعدة استعمالات تخص البيتكوين منها

 - يمكن استغلاله كمحفظة باردة مؤقته غير متصله بالانترنت لتوقيع عمليات بيتكوين داخل نظام التشغيل هذا بشكل معزول عن الانترنت وبدون ترك اي تفاصيل على حاسوبك.
- يمكنك استعماله كجزء من محفظة متعددة التواقيع.
- حساب الكلمة المفتاحية الأخيرة او ما تعرف بال Checksum التي بحاجة لحساب الهاش Link بعد إنشاء [كلمات مفتاحية](/wallets/#ما-هي-الكلمات-المفتاحية) بشكل يدوي (مثلا رمي قطعى نقدية او رمي حجر نرد - لإنشاء عشوائية بشكل يدوي) 
- يمكنك انشاء محفظة أُم بنظام bip85 واستخراج الكلمات المفتاحية لاحد محافظ الابناء (Index) بشكل امن ومعزل عن الانترنت
- استخراج ال [XPUB](/wallets/#ما-هو-ال-xpub) لمحفظة بعد ادخال الكلمات المفتاحية في نظام Tails
- يمكنك استعمالة لحساب XOR لكلمات مفتاحية.

والعديد العديد من استعمالات البيتكوين السرية بطريقة امنه ومعزولة عن الانترنت.

 ::: tip Pro Tip 😎 تيب معلمين
 كما سترى في هذا الدليل انت لست بحاجة لحاسوب اخر اذ يمكنك استعمال حاسوبك الشخصي الحالي الذي تمتلكه. لكن اذا كنت تمتلك حاسوب قديم اخر لم تعد تستعمله يمكنك إحيائه من جديد واستعماله كمحفظة باردة معزوله تماما عن العالم الخارجي عن طريق:
 - ازالة القرص الصلب منه فيزيائيا.
 - فصل كرت الانترنت الوافي وفصل كرت البلوتوث. 
::: 
  
## 🔘كيفية تثبيت نظام  Tails على قرص USB
يمكن تثبيت نظام Tails على أي قرص USB بسعة 8GB على الأقل. أنتبه عند تثبيت النظام على قرص الفلاشة USB Flash Drive سيتم حذف جميع محتوى القرص.
### 🔸 ما هي متطلبات النظام وجهاز الحاسوب
- قرص USB بسعة 8GB على الأقل (يُفضل USB3 وما فوق لانه أسرع).
- حاسوب يحتوي على ذاكرة عشوائية RAM بسعة 2GB على الأقل.
### 🔸 تحميل نظام Tails
طريقة التحميل الاسهل هي عبر تنزيل نظام Tails من الموقع الرسمي  [https://tails.boum.org](https://tails.boum.org/install/index.en.html) 

::: warning هناك طرق اخرى لتحميل نظام Tails
+ يمكنك تحميل Tails أيضا من خلال BitTorrent شاهد [التفاصيل هنا](https://tails.boum.org/torrents/).
+ كما ويمكنك نسخ وتنصيب Tails من قرص فلاشة اخر USB Flash Drive منصب عليه نظام Tails (مثلا من صديق تثق به) 
	+ [لاستنساخ Tails من قرص USB اخر باستخدام جهاز حاسوب عادي PC](https://tails.boum.org/install/clone/pc/index.en.html)
	+ [ لاستنساخ Tails من قرص USB اخر باستخدام جهاز حاسوب Mac](https://tails.boum.org/install/clone/mac/index.en.html)
:::

#### اليكم الخطوات:
![Tails](/images/tails-os/all_steps.png)

1. قم بالدخول الى الموقع  <https://tails.boum.org/install/index.en.html>  ثم قم بتحديد نظام التشغيل الحالي الخاص بك الذي تستخدمه الان (كنظام الويندوز مثلا):

![Tails](/images/tails-os/install_tails_1.png)

2. قم بالضغط على زر التحميل الأخضر  Download Tails كما بالصورة التالية:

![Tails](/images/tails-os/download.png)

3. بعد الانتهاء من تحميل الملف قم بالضغط على الزر الاخضر Select your download…  كما بالصورة واختر الملف لكي يتم التأكد من صحة محتواه

![Tails](/images/tails-os/verify.png)

![Tails](/images/tails-os/verify_1.png)

بعد الانتهاء ستظهر لك هذة الرسالة `Verification successful`:
![Tails](/images/tails-os/verify_2.png)


::: warning أنتباه
بالإضافة للخطوة السابقة انصحكم بالتحقق من الملف ايضا  عبر  PGP  اذا كنت لا تعرف كيف تتم هذة العملية انصحك بقراءة [هذا المقال اولا](verify-files-with-gpg.html)

::: details اضغط هنا لمعرفة الطريقة باختصار
- اولا قم بالدخول مجددا للموقع <https://tails.boum.org/install/index.en.html> 
- هذة المرة <Badge text="انتبه" vertical ="top"  type="warning"/>  ان هنالك رابط اسفل الزر الاخضر `or verify using the OpenPGP signature` اضغط عليه.
![Tails](/images/tails-os/verify_using_gpg.png)
- سيتم فتح الصورة التالية، قم بتحميل التوقيع والمفتاح العام:
![Tails](/images/tails-os/verify_using_gpg_1.png)
- الان اصبح لديك 3 ملفات: 
	- ملف المفتاح العام للمطور  `tails-signing.key`
	- ملف التوقيع `tails-amd64-5.12.img.sig`
	- ملف نظام التشغيل `tails-amd64-5.12.img`

- قم بجلب المفتاح العام عبر تطبيق [kleopatra](verify-files-with-gpg.html#تثبيت-gpg-في-windows) عن طريق اختيار `import`  اختر اظهار كل انواع الملفات بالاسفل `Any files` واختر الملف `tails-signing.key` من المجلد الصحيح

![Tails](/images/tails-os/verify_using_gpg_2.png)
 لاحظ انه تم إضافة المفتاح العام التالي للتطبيق (انتبه لاخر  16 خانة في المفتاح الثاني)
 
```
Primary key fingerprint: A490 D0F4 D311 A415 3E2B  B7CA DBB8 02B2 58AC D84F
Subkey fingerprint: CD4D 4351 AFA6 933F 574A  9AFB 90B2 B4BD 7AED 235F
```
![Tails](/images/tails-os/verify_using_gpg_3.png)
- نعود للمجلد الرئيسي ونقوم بفتح الملف `tails-amd64-5.12.img.sig` سيفتح [برنامج كليوباترا](verify-files-with-gpg.html#تثبيت-gpg-في-windows) ويتحقق من الملف تلقائيا:
![Tails](/images/tails-os/verify_using_gpg_4.png)
لاحظ اننا حصلنا على توقيع سليم من المطور `Good signature`

```bash
Good signature from "Tails developers <tails@boum.org>"
```
![Tails](/images/tails-os/verify_using_gpg_5.png)

**الان يمكنك الانتقال الى الخطوة التالية وتنصيب نظام التشغيل**
:::


4. تحميل برنامج balenaEtcher  عن طريق الضغط على الزر `Download balenaEtcher for Windows`

![Tails](/images/tails-os/download_balenaetcher.png)

قم بتنصيبه ومن ثم فتحه لتظهر لك هذة الشاشة:

![Tails](/images/tails-os/etcher_in_windows.png)


5. بعدها قم بادخال قرص ال USB  الى الحاسوب

انتبه  سيتم حذف جميع محتوى قرص ال USB - تأكد من استعمال USB جديد او فارغ.

- قم بالضغط على `Flash from file` واختر ملف نظام التشغيل `tails-amd64-5.12.img`
- قم بالضغط على `Select target ` واختر قرص ال USB
- قم بالضغط على `Flash` 

![Tails](/images/tails-os/balena-etcher.gif)

انتهيت الان اصبح لديك نظام تشغيل Tails على ال DiskOnKey جاهز للاستعمال

![Tails](/images/tails-os/laptop.svg)

**اغلق جهاز الحاسوب وقم بتشغيله مرة اخرى وتأكد من أن يكون قرص الUSB موصل بالحاسوب**. 

اذا اشتغل نظام التشغيل السابق(الوينوز في مثالنا وليس Tails). انتقل الى الخطوة التالية لتغيير إعدادات الحاسوب لكي يبدأ من قرص ال USB

6 . تعيين الحاسوب لكي يبدأ من قرص ال USB بدلا من القرص الصلب

في العادة يكون الحاسوب مبرمج مسبقا لكي يبدأ من القرص الصلب اولا، لكن نحن نريده ان يبدأ من ال USB لذلك علينا تغيير إعدادات بدأ النظام ( Boot Menu).

::: details الطريقة الأولى هي من داخل ويندوز إضغط هنا للمزيد

**في ويندوز يمكن تغيير اعدادات الحاسوب داخل ويندوز لكي يبدأ من قرص ال USB في المرة القادمة من خلال الضغط على :**

 ![Tails](/images/tails-os/start.png) -> اضغط باستمرار على مفتاح**Shift** ثم **Power** ثم **Restart(إعادة التشغيل)**.

قم باختيار `Use a device.`

![Tails](/images/tails-os/choose_an_option.png)

:::
اذا لم تنجح هذة الطريقة اعلاه عليك معرفة ما هو الزر  في لوحة المفاتيح الذي يمكنه دخول ال ( Boot Menu) في حاسوبك. يمكنك البحث في محرك البحث عن:
```ts
# how to enter boot menu <اكتب نوع حاسوبك> 
how to enter boot menu dell latitude 5420
```

اغلق الحاسوب مرة اخرى. هذة المرة عند تشغيل الحاسوب قم بالضغط عدة مرات متتالية على أحد هذة الأزرار من القائمة ادناة حسب نوع حاسوب 

#### قائمة بانواع الحواسيب والمفتاح الخاص بلوحة المفاتيح الذي يدخل على اعدادات ال ( Boot Menu)

| نوع الحاسوب | المفتاح بلوحة المفاتيح |
| --- | --- | 
|	Acer |	F12, F9, F2, Esc |
|Apple	| Option |
| Asus	| Esc|
| Clevo	|F7                          |
| Dell	|F12                        |
| Fujitsu	|F12, Esc             |
| HP|	F9                              |
| Huawei|	F12                    |
| Intel|	F10                        |
| Lenovo|	F12                    |
| MSI |	F11                        |
| Samsung	| Esc, F12, F2   |
| Sony	|F11, Esc, F10         |
| Toshiba |	F12                    |
| others…	|F12, Esc             |

 ::: tip Pro Tip 😎 تيب معلمين
يمكنك تعديل هذة الخاصية بشكل دائم في البيوس BIOS
ابحث في الانترنت كيف يمكنك تعديل اعدادات البيوس BIOS في حاسوبك ليقوم دائما بالدخول الى نظام التشغيل من قرص ال USB.
:::

ستظهر لكم نافذة كالتالي:

![Tails](/images/tails-os/boot_menu.png)

قم باختيار `Tails`:

![Tails](/images/tails-os/grub.png)

انتظروا بضع دقائق

![Tails](/images/tails-os/plymouth.png)

ستظهر لكم صفحة البداية

![Tails](/images/tails-os/welcome_screen.png)

> اذا اردت العمل Offline يمكنكم إلغاء الإنترنت بتاتا عن نظام التشغيل من خلال الضغط على `+` في خانة `Additional Settings` ومن ثم `Offline Mode`  ومن ثم `Disable all networking` وبعدها نبدأ تشغيل النظام بالضغط على `Start Tails`
![Tails](/images/tails-os/Tails_offline_mode.gif)

وهذة هي صفحة سطح المكتب في Tails
![Tails](/images/tails-os/desktop.png)

## فيديو يشرح نظام تشغيل Tails
هذا فيديو يشرح لكم عن نظام تشغيل Tails باللغة الانجليزية
[![Introduction to Tails](/images/tails-os/tails_video.png)](https://yewtu.be/watch?v=-f6cgUKBUXg "Introduction to Tails")

وهذا فيديو اخر يشرح لماذا هذا النظام مناسب ايضا للمستخدمين العاديين مثلي ومثلك وليس فقط للصحفيين وكاشفي الفساد والمحتاجين بشدة للسرية والخصوصية
[![Why Tails is not only for hacktivists and whistleblowers and how to get started](/images/tails-os/tails_video_2.png)](https://yewtu.be/watch?v=kZ4NHz-gjLo "Why Tails is not only for hacktivists and whistleblowers and how to get started")