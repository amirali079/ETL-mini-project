# ETL-mini-project


<div dir='rtl' align="center">
به نام پروردگار هدایت‌کننده به راه راست
 مستند پروژه ارزیابی ورودی تیم DIA
</div>
  <div dir="rtl" align='right'>

## مقدمه
در این پروژه از شما می‌خواهیم تا یک نرم‌افزار ETL پیاده‌سازی کنید. در ادامه به بیان نیازمندی‌ها می‌پردازیم.
اگر تاکنون با مفهوم ETL آشنا نیستید یا نیاز به اطلاعات تکمیلی دارید می‌توانید از طریق این لینک مطالعه کنید.
## کلیات
روزانه مقادیری داده در قالب جدول‌های SQL و یا فایل‌های CSV   به‌دست ما می‌رسد که نیاز است روی آن‌ها پردازش‌هایی انجام شود و نتیجه‌ی به دست آمده را توسط API‌ها برگردانیم.
یعنی در نهایت ما تعدادی API داریم که با گرفتن داده‌های ورودی، پردازش‌های مورد نظر را روی آن‌ها انجام داده و داده‌های پردازش شده را در خروجی API برمی‌گرداند.
جداول یا فایل‌های ورودی لزوماً فرمت و ستون‌های یکسانی ندارند و بر حسب نیاز ممکن است ستون‌های متفاوتی داشته باشند.
بخش‌های مختلف پروژه به‌صورت زیر است :
 
## پردازش‌های ورودی
این دسته از پردازش‌ها به کاربر این امکان را می‌دهد تا داده‌ی ورودی خود را به نرم‌افزار وارد کند.
### خواندن از جدول
این پردازش به کاربر این امکان را می‌دهد تا به یک پایگاه داده‌ی PostgreSQL وصل شود و یکی از جدول‌ها آن را انتخاب نماید و داده‌های آن را دریافت نماید تا بتوان در پردازش‌های دیگر از آن داده‌ها استفاده کرد. توجه شود که کاربر باید بتواند پایگاه داده‌ی PostgreSQL  مورد نظر خود را با تعیین آدرس سرور و نام کاربری و کلمه‌ی عبور تعیین کند. سپس بتواند نام پایگاه‌های داده و جداول موجود را مشاهده و جدول مورد نظر را انتخاب کند.
نکته : می‌توان بجای کار با PostgreSQL  از SQL Server استفاده نمود.
### خواندن از فایل CSV
با این پردازش می‌توان محتوای یک فایل CSV را دریافت کرد و در ادامه بتوان از آن داده در پردازش‌های دیگر استفاده کرد.
## پردازش‌های میانی
این پردازش‌ها یک ساختار جدولی به عنوان ورودی دریافت می‌کنند و یک ساختار جدولی برای استفاده در سایر پردازش‌ها خروجی می‌دهند.
 
### پردازش فیلتر ستونی
در این پردازش می‌توان روی داده‌های یک ساختار جدولی فیلتر اعمال کرد. به این صورت که می‌توان روی هر ستون شروطی گذاشت که سطرهایی که در آن شروط صدق می‌کنند به عنوان خروجی تولید شوند. شرط‌ها می‌توانند روی ستون‌های مختلف اعمال شوند و روی هر ستون هم ممکن است چندین شرط تعریف شود. ارتباط منطقی شرط‌ها می‌تواند AND یا OR باشد. در نتیجه کاربر می‌تواند درختی از شرط‌ها را تعریف کند که در آن هر یک از برگ‌ها یک شرط روی یک ستون را نمایش می‌دهد و سایر رأس‌ها بیانگر AND یا OR هستند. در شکل زیر می‌توانید یک نمونه از این درخت را مشاهده کنید.
شرط‌های قابل اعمال:
·        برای همه‌ی انواع داده‌های متنی و عدد صحیح:
o       برابر باشد با
·        برای ستون‌های عددی:
o       کوچکتر باشد از
o       بزرگ‌تر باشد از
 
### پردازش تجمیع سازی
در این پردازش یک ساختار جدولی به عنوان ورودی گرفته می‌شود و یک ساختار جدولی هم خروجی آن است. کاربر می‌تواند یکی از انواع Aggregation را انتخاب کند و تعدادی از ستون‌ها را هم برای گروه‌بندی انتخاب کند.
Aggregation های زیر مورد نیاز است:
<div dir='ltr' align="justify">
+ COUNT
+ SUM
+ AVERAGE
+ MIN
+ MAX
 </div>

 
## نکات پیاده‌سازی :
پروژه زیر شامل زیرساخت Back-End بوده و نیازی به طراحی رابط کاربری Front-End نیست.
خروجی کار باید از طریق API های طراحی شده قابل مشاهده باشد.
پروژه باید با فریمورک .Net  پیاده‌سازی شود و استفاده از کتابخانه‌های مرتبط با آن مجاز می‌باشد.
برای بخش‌های مختلف پروژه Unit Test , Integration Test  باید نوشته شود و جز نکات کلیدی ارزیابی است.
طراحی معماری صحیح، کلاس‌بندی صحیح، رعایت اصول‌شی‌گرایی، رعایت اصول کدنویسی تمیز نیز جزو نکات ارزیابی است.
طراحی‌ معماری و ساختار API ها بر عهده شما می‌باشد.

</div>
