<div dir="rtl">
> انتهى Appwrite Init! يمكنك الاطلاع على جميع الإعلانات الأخيرة [على موقع Init الخاص بنا](https://appwrite.io/init) :rocket:

<br />
<p align="center">
    <a href="https://appwrite.io" target="_blank"><img src="./public/images/banner.png" alt="لافتة Appwrite، مع شعار ونص يقول "قم بالبناء مثل فريق من المئات"></a>
    <br />
    <br />
    <b>Appwrite عبارة عن منصة خلفية لتطوير تطبيقات الويب والجوال وFlutter. تم إنشاؤها بالتعاون مع مجتمع المصدر المفتوح وتم تحسينها لتلائم تجربة المطورين في لغات البرمجة التي تحبها.</b>
    <br />
    <br />
</p>

<!-- [![Build Status](https://img.shields.io/travis/com/appwrite/appwrite?style=flat-square)](https://travis-ci.com/appwrite/appwrite) -->

[![We're Hiring label](https://img.shields.io/static/v1?label=We're&message=Hiring&color=blue&style=flat-square)](https://appwrite.io/company/careers)
[![Hacktoberfest label](https://img.shields.io/static/v1?label=hacktoberfest&message=ready&color=191120&style=flat-square)](https://hacktoberfest.appwrite.io)
[![Discord label](https://img.shields.io/discord/564160730845151244?label=discord&style=flat-square)](https://appwrite.io/discord?r=Github)
[![Build Status label](https://img.shields.io/github/actions/workflow/status/appwrite/appwrite/tests.yml?branch=master&label=tests&style=flat-square)](https://github.com/appwrite/appwrite/actions)
[![X Account label](https://img.shields.io/twitter/follow/appwrite?color=00acee&label=twitter&style=flat-square)](https://twitter.com/appwrite)

<!-- [![Docker Pulls](https://img.shields.io/docker/pulls/appwrite/appwrite?color=f02e65&style=flat-square)](https://hub.docker.com/r/appwrite/appwrite) -->
<!-- [![Translate](https://img.shields.io/badge/translate-f02e65?style=flat-square)](docs/tutorials/add-translations.md) -->
<!-- [![Swag Store](https://img.shields.io/badge/swag%20store-f02e65?style=flat-square)](https://store.appwrite.io) -->
عربي | [English](README.md) | [简体中文](README-CN.md)

[**الإعلان عن الإصدار التجريبي العام من Appwrite Cloud! سجل اليوم!**](https://cloud.appwrite.io)

Appwrite هو خادم خلفي شامل لتطبيقات الويب أو الأجهزة المحمولة أو التطبيقات الأصلية أو الخلفية، يتم تجميعه كمجموعة من الخدمات المصغرة Docker. يلخص Appwrite التعقيد والتكرار المطلوب لبناء واجهة برمجة تطبيقات خلفية حديثة من الصفر ويسمح لك ببناء تطبيقات آمنة بشكل أسرع.

باستخدام Appwrite، يمكنك بسهولة دمج تطبيقك مع مصادقة المستخدم وطرق تسجيل الدخول المتعددة، وقاعدة بيانات لتخزين واستعلام بيانات المستخدمين والفريق، وإدارة التخزين والملفات، والتلاعب بالصور، ووظائف السحابة، و[المزيد من الخدمات](https://appwrite.io/docs).

<p align="center">
    <br />
    <a href="https://www.producthunt.com/posts/appwrite-2?utm_source=badge-top-post-badge&utm_medium=badge&utm_souce=badge-appwrite-2" target="_blank"><img src="https://api.producthunt.com/widgets/embed-image/v1/top-post-badge.svg?post_id=360315&theme=light&period=daily" alt="Appwrite - 100% مصدر مفتوح بديل لـ Firebase | Product Hunt" style="width: 250px; height: 54px;" width="250" height="54" /></a>
    <br />
    <br />
</p>

![لوحة معلومات مشروع Appwrite تعرض ميزات Appwrite المختلفة](public/images/github.png)

لمعرفة المزيد، تفضل بزيارة: [https://appwrite.io](https://appwrite.io).

جدول المحتويات:

- [البدء](#getting-started)
- [استضافة ذاتية](#self-hosting)
  - [يونكس](#unix)
  - [ويندوز](#windows)
    - [CMD](#cmd)
    - [PowerShell](#powershell)
  - [الترقية من إصدار أقدم](#upgrade-from-an-older-version)
- [إعدادات بنقرة واحدة](#one-click-setups)
- [البدء](#getting-started)
  - [الخدمات](#services)
  - [مجموعات تطوير البرامج](#sdks)
    - [عميل](#client)
    - [خادم](#server)
    - [المجتمع](#community)
- [هندسة معمارية](#architecture)
- [المساهمة](#contributing)
- [الأمان](#security)
- [تابعنا](#follow-us)
- [ترخيص](#license)

## ابدء
الطريقة الأسهل للبدء في استخدام Appwrite هي [التسجيل في Appwrite Cloud](https://cloud.appwrite.io/). وبينما Appwrite Cloud في مرحلة تجريبية عامة، يمكنك البناء باستخدام Appwrite مجانًا تمامًا، ولن نجمع معلومات بطاقتك الائتمانية.

## الاستضافة الذاتية

تم تصميم Appwrite للعمل في بيئة حاويات. تشغيل الخادم الخاص بك سهل مثل تشغيل أمر واحد من محطتك الطرفية. يمكنك تشغيل Appwrite على localhost الخاص بك باستخدام docker-compose أو على أي أداة أخرى لتنظيم الحاويات، مثل [Kubernetes](https://kubernetes.io/docs/home/)، [Docker Swarm](https://docs.docker.com/engine/swarm/)، أو [Rancher](https://rancher.com/docs/).

قبل تشغيل أمر التثبيت، تأكد من تثبيت [Docker](https://www.docker.com/products/docker-desktop) على جهازك:

### يونيكس

```bash
docker run -it --rm \
    --volume /var/run/docker.sock:/var/run/docker.sock \
    --volume "$(pwd)"/appwrite:/usr/src/code/appwrite:rw \
    --entrypoint="install" \
    appwrite/appwrite:1.6.0
```

### الويندوز

#### أمر الأوامر

```cmd
docker run -it --rm ^
    --volume //var/run/docker.sock:/var/run/docker.sock ^
    --volume "%cd%"/appwrite:/usr/src/code/appwrite:rw ^
    --entrypoint="install" ^
    appwrite/appwrite:1.6.0
```

#### باورشيل

```powershell
docker run -it --rm `
    --volume /var/run/docker.sock:/var/run/docker.sock `
    --volume ${pwd}/appwrite:/usr/src/code/appwrite:rw `
    --entrypoint="install" `
    appwrite/appwrite:1.6.0
```

بمجرد اكتمال تثبيت Docker، انتقل إلى http://localhost للوصول إلى وحدة تحكم Appwrite من متصفحك. يرجى ملاحظة أنه على المضيفات غير الأصلية التي تعمل بنظام Linux، قد يستغرق الخادم بضع دقائق للبدء بعد إكمال التثبيت.

للإنتاج المتقدم والتثبيت المخصص، راجع مستندات Docker [متغيرات البيئة](https://appwrite.io/docs/environment-variables). يمكنك أيضًا استخدام ملفاتنا العامة [docker-compose.yml](https://appwrite.io/install/compose) و[.env](https://appwrite.io/install/env) لإعداد بيئة يدويًا.

### الترقية من إصدار أقدم

إذا كنت تقوم بترقية خادم Appwrite الخاص بك من إصدار أقدم، فيجب عليك استخدام أداة ترحيل Appwrite بمجرد اكتمال الإعداد. لمزيد من المعلومات بخصوص هذا الأمر، راجع [وثائق التثبيت](https://appwrite.io/docs/self-hosting).

## إعدادات بنقرة واحدة

بالإضافة إلى تشغيل Appwrite محليًا، يمكنك أيضًا تشغيل Appwrite باستخدام إعداد مُهيأ مسبقًا. يتيح لك هذا البدء في التشغيل بسرعة باستخدام Appwrite دون تثبيت Docker على جهازك المحلي.

اختر من أحد مقدمي الخدمة أدناه:

<table border="0">
  <tr>
    <td align="center" width="100" height="100">
      <a href="https://marketplace.digitalocean.com/apps/appwrite">
        <img width="50" height="39" src="public/images/integrations/digitalocean-logo.svg" alt="شعار DigitalOcean" />
          <br /><sub><b>DigitalOcean</b></sub></a>
        </a>
    </td>
    <td align="center" width="100" height="100">
      <a href="https://gitpod.io/#https://github.com/appwrite/integration-for-gitpod">
        <img width="50" height="39" src="public/images/integrations/gitpod-logo.svg" alt="شعار Gitpod" />
          <br /><sub><b>Gitpod</b></sub></a>    
      </a>
    </td>
    <td align="center" width="100" height="100">
      <a href="https://www.linode.com/marketplace/apps/appwrite/appwrite/">
        <img width="50" height="39" src="public/images/integrations/akamai-logo.svg" alt="شعار Akamai" />
          <br /><sub><b>Akamai Compute</b></sub></a>    
      </a>
    </td>
    <td align="center" width="100" height="100">
      <a href="https://aws.amazon.com/marketplace/pp/prodview-2hiaeo2px4md6">
        <img width="50" height="39" src="public/images/integrations/aws-logo.svg" alt="شعار AWS" />
          <br /><sub><b>AWS Marketplace</b></sub></a>    
      </a>
    </td>
  </tr>
</table>

## ابدء

إن البدء في استخدام Appwrite أمر سهل للغاية، حيث يتطلب إنشاء مشروع جديد واختيار المنصة المناسبة ودمج مجموعة أدوات التطوير البرمجية الخاصة به في الكود الخاص بك. ويمكنك بسهولة البدء في استخدام المنصة التي تختارها من خلال قراءة أحد دروسنا التعليمية حول البدء.

| المنصة              | التقنية                                                                         |
| --------------------- | ---------------------------------------------------------------------------------- |
| **تتطبيق ويب**           | [بدء سريع للويب](https://appwrite.io/docs/quick-starts/web)                   |
|                       | [بدء سريع بـ Next.js](https://appwrite.io/docs/quick-starts/nextjs)            |
|                       | [بدء سريع بـ React](https://appwrite.io/docs/quick-starts/react)               |
|                       | [بدء سريع بـ Vue.js](https://appwrite.io/docs/quick-starts/vue)                |
|                       | [بدء سريع بـ Nuxt](https://appwrite.io/docs/quick-starts/nuxt)                 |
|                       | [بدء سريع بـ SvelteKit](https://appwrite.io/docs/quick-starts/sveltekit)       |
|                       | [بدء سريع بـ Refine](https://appwrite.io/docs/quick-starts/refine)             |
|                       | [بدء سريع بـ Angular](https://appwrite.io/docs/quick-starts/angular)           |
| **تطبيقات المحمول** | [بدء سريع بـ React Native](https://appwrite.io/docs/quick-starts/react-native) |
|                       | [بدء سريع بـ Flutter](https://appwrite.io/docs/quick-starts/flutter)           |
|                       | [بدء سريع بـ Apple](https://appwrite.io/docs/quick-starts/apple)               |
|                       | [بدء سريع بـ Android](https://appwrite.io/docs/quick-starts/android)           |
| **الخادوم**            | [بدء سريع بـ Node.js](https://appwrite.io/docs/quick-starts/node)              |
|                       | [بدء سريع بـ Python](https://appwrite.io/docs/quick-starts/python)             |
|                       | [بدء سريع بـ .NET](https://appwrite.io/docs/quick-starts/dotnet)               |
|                       | [بدء سريع بـ Dart](https://appwrite.io/docs/quick-starts/dart)                 |
|                       | [بدء سريع بـ Ruby](https://appwrite.io/docs/quick-starts/ruby)                 |
|                       | [بدء سريع بـ Deno](https://appwrite.io/docs/quick-starts/deno)                 |
|                       | [بدء سريع بـ PHP](https://appwrite.io/docs/quick-starts/php)                   |
|                       | [بدء سريع بـ Kotlin](https://appwrite.io/docs/quick-starts/kotlin)             |
|                       | [بدء سريع بـ Swift](https://appwrite.io/docs/quick-starts/swift)               |
### منتجات

- [**الحساب**](https://appwrite.io/docs/references/cloud/client-web/account) - إدارة مصادقة المستخدم الحالي والحساب. تتبع وإدارة جلسات المستخدم والأجهزة وطرق تسجيل الدخول وسجلات الأمان.
- [**المستخدمون**](https://appwrite.io/docs/server/users) - إدارة وإدراج جميع مستخدمي المشروع عند بناء تكاملات خلفية مع مجموعات SDK الخاصة بالخادم.
- [**الفرق**](https://appwrite.io/docs/references/cloud/client-web/teams) - إدارة المستخدمين وتجميعهم في فرق. إدارة العضويات والدعوات وأدوار المستخدم داخل الفريق.
- [**قواعد البيانات**](https://appwrite.io/docs/references/cloud/client-web/databases) - إدارة قواعد البيانات والمجموعات والمستندات. قراءة وإنشاء وتحديث وحذف المستندات وتصفية قوائم مجموعات المستندات باستخدام المرشحات المتقدمة.
- [**التخزين**](https://appwrite.io/docs/references/cloud/client-web/storage) - إدارة ملفات التخزين. قراءة الملفات وإنشاؤها وحذفها ومعاينتها. معالجة معاينة ملفاتك لتناسب تطبيقك تمامًا. يتم فحص جميع الملفات بواسطة ClamAV وتخزينها بطريقة آمنة ومشفرة.
- [**Functions**](https://appwrite.io/docs/references/cloud/server-nodejs/functions) - قم بتخصيص مشروع Appwrite الخاص بك من خلال تنفيذ الكود المخصص في بيئة آمنة ومعزولة. يمكنك تشغيل الكود الخاص بك في أي حدث نظام Appwrite إما يدويًا أو باستخدام جدول CRON.
- [**المراسلة**](https://appwrite.io/docs/references/cloud/client-web/messaging) - تواصل مع المستخدمين من خلال الإشعارات الفورية ورسائل البريد الإلكتروني والرسائل النصية القصيرة باستخدام Appwrite Messaging.
- [**الوقت الحقيقي**](https://appwrite.io/docs/realtime) - استمع إلى الأحداث في الوقت الحقيقي لأي من خدمات Appwrite الخاصة بك بما في ذلك المستخدمين والتخزين والوظائف وقواعد البيانات والمزيد.
- [**Locale**](https://appwrite.io/docs/references/cloud/client-web/locale) - تتبع موقع المستخدم وإدارة بيانات تطبيقك المستندة إلى الموقع المحلي.
- [**الصور الرمزية**](https://appwrite.io/docs/references/cloud/client-web/avatars) - يمكنك إدارة الصور الرمزية للمستخدمين وأعلام الدول وأيقونات المتصفح ورموز بطاقات الائتمان. يمكنك إنشاء أكواد QR من الروابط أو سلاسل النصوص العادية.

للحصول على وثائق API الكاملة، تفضل بزيارة [https://appwrite.io/docs](https://appwrite.io/docs). لمزيد من البرامج التعليمية والأخبار والإعلانات، راجع [مدونتنا](https://medium.com/appwrite-io) و[خادم Discord](https://discord.gg/GSeTUeA).

### حزم تطوير البرامج

فيما يلي قائمة بالمنصات واللغات المدعومة حاليًا. إذا كنت ترغب في مساعدتنا في إضافة الدعم إلى المنصة التي تختارها، يمكنك الانتقال إلى مشروعنا [SDK Generator](https://github.com/appwrite/sdk-generator) وعرض [دليل المساهمة](https://github.com/appwrite/sdk-generator/blob/master/CONTRIBUTING.md).

#### عميل

- :white_check_mark:   [الويب](https://github.com/appwrite/sdk-for-web) (تتم صيانته بواسطة فريق Appwrite)
- :white_check_mark:   [Flutter](https://github.com/appwrite/sdk-for-flutter) (تتم صيانته بواسطة فريق Appwrite)
- :white_check_mark:   [Apple](https://github.com/appwrite/sdk-for-apple) (تحت إشراف فريق Appwrite)
- :white_check_mark:   [Android](https://github.com/appwrite/sdk-for-android) (تتم صيانته بواسطة فريق Appwrite)
- :white_check_mark:   [React Native](https://github.com/appwrite/sdk-for-react-native) - **إصدار تجريبي** (تحت إدارة فريق Appwrite)

#### الخادم

- :white_check_mark:   [NodeJS](https://github.com/appwrite/sdk-for-node) (تتم صيانته بواسطة فريق Appwrite)
- :white_check_mark:   [PHP](https://github.com/appwrite/sdk-for-php) (تتم صيانته بواسطة فريق Appwrite)
- :white_check_mark:   [Dart](https://github.com/appwrite/sdk-for-dart) (تتم صيانته بواسطة فريق Appwrite)
- :white_check_mark:   [Deno](https://github.com/appwrite/sdk-for-deno) (تتم صيانته بواسطة فريق Appwrite)
- :white_check_mark:   [Ruby](https://github.com/appwrite/sdk-for-ruby) (تتم صيانته بواسطة فريق Appwrite)
- :white_check_mark:   [Python](https://github.com/appwrite/sdk-for-python) (تتم صيانته بواسطة فريق Appwrite)
- :white_check_mark: [Kotlin](https://github.com/appwrite/sdk-for-kotlin) (تتم صيانته بواسطة فريق Appwrite)
- :white_check_mark:   [Swift](https://github.com/appwrite/sdk-for-swift) (تتم صيانته بواسطة فريق Appwrite)
- :white_check_mark:   [.NET](https://github.com/appwrite/sdk-for-dotnet) - **إصدار تجريبي** (تحت إدارة فريق Appwrite)

#### مجتمع

- :white_check_mark: [Appcelerator Titanium](https://github.com/m1ga/ti.appwrite) (تحت إشراف [Michael Gangolf](https://github.com/m1ga/))
- :white_check_mark: [محرك Godot](https://github.com/GodotNuts/appwrite-sdk) (تتم صيانته بواسطة [fenix-hub @GodotNuts](https://github.com/fenix-hub))

هل تبحث عن المزيد من حزم SDK؟ - ساعدنا من خلال المساهمة في طلب سحب إلى [مولد SDK] (https://github.com/appwrite/sdk-generator) الخاص بنا!

## بنيان

![هندسة Appwrite التي توضح كيفية بناء Appwrite والخدمات والأدوات التي يستخدمها](docs/specs/overview.drawio.svg)

يستخدم Appwrite بنية خدمات مصغرة تم تصميمها لتسهيل التوسع وتفويض المسؤوليات. بالإضافة إلى ذلك، يدعم Appwrite واجهات برمجة تطبيقات متعددة، مثل REST وWebSocket وGraphQL للسماح لك بالتفاعل مع مواردك من خلال الاستفادة من معرفتك الحالية وبروتوكولاتك المفضلة.

تم تصميم طبقة واجهة برمجة التطبيقات Appwrite لتكون سريعة للغاية من خلال الاستفادة من التخزين المؤقت في الذاكرة وتفويض أي مهام ثقيلة إلى عمال الخلفية Appwrite. كما يسمح لك عمال الخلفية بالتحكم بدقة في سعة الحوسبة والتكاليف باستخدام قائمة رسائل للتعامل مع الحمل. يمكنك معرفة المزيد عن بنيتنا في [دليل المساهمة](CONTRIBUTING.md#architecture-1).

## المساهمة

يجب أن تمر جميع مساهمات الكود، بما في ذلك مساهمات الأشخاص الذين لديهم حق الوصول إلى الالتزام، بطلب سحب وأن تتم الموافقة عليها من قبل مطور أساسي قبل دمجها. وهذا لضمان المراجعة المناسبة لكل الكود.

نحن نرحب حقًا بطلبات السحب! إذا كنت ترغب في المساعدة، يمكنك معرفة المزيد حول كيفية المساهمة في هذا المشروع في [دليل المساهمة](CONTRIBUTING.md).

## حماية

بالنسبة لمشاكل الأمان، يرجى مراسلتنا عبر البريد الإلكتروني على [security@appwrite.io](mailto:security@appwrite.io) بدلاً من نشر مشكلة عامة على GitHub.

## تابعنا

انضم إلى مجتمعنا المتنامي حول العالم! اطلع على [مدونتنا](https://appwrite.io/blog) الرسمية. تابعنا على [X](https://twitter.com/appwrite)، [LinkedIn](https://www.linkedin.com/company/appwrite/)، [Dev Community](https://dev.to/appwrite) أو انضم إلى [خادم Discord](https://appwrite.io/discord) المباشر الخاص بنا للحصول على المزيد من المساعدة والأفكار والمناقشات.

## رخصة

يتوفر هذا المستودع بموجب [رخصة BSD 3-Clause](./LICENSE).
