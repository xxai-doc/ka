<p align="center"><a href="https://xxai.art"><img src="https://cdn.jsdelivr.net/gh/xxai-art/doc/logo.svg"/></a><br/><a href="https://xxai.art"><img src="https://cdn.jsdelivr.net/gh/xxai-art/doc/xxai.svg"/></a></p><p align="center"><a href="https://github.com/xxai-art/doc#readme"><img alt="I18N" src="https://cdn.jsdelivr.net/gh/wactax/img/t.svg"/></a>　<a href="https://groups.google.com/u/0/g/xxai-art"><img alt="Google Groups" src="https://cdn.jsdelivr.net/gh/wactax/img/g-groups.svg"/></a></p>

# xxAI.ხელოვნება

ვებსაიტის კოდის ნაწილი ღია წყაროა, კეთილი იყოს თქვენი მობრძანება თარგმანის ოპტიმიზაციაში.

## წინა ბოლო კოდი

* [წინა ბოლო კოდი](https://github.com/xxai-art/web)
* [ენების პაკეტები მთლიანად საიტისთვის](https://github.com/xxai-art/web/tree/main/i18n)
* [ენის პაკეტები შესვლის მოდულებისთვის](https://github.com/wacpkg/user/tree/main/ui.i18n)
* [ვებსაიტის მრავალენოვანი დოკუმენტაცია](https://github.com/xxai-doc)

წინა პროგრამირების ენაა [@w5/coffee_plus](http://npmjs.com/@w5/coffee_plus) , რომელიც ამატებს ზოგიერთ მახასიათებელს coffeescript სინტაქსის საფუძველზე, იხილეთ [./coffee_plus.md](./coffee_plus.md) .

## ვებსაიტების და დოკუმენტების ინტერნაციონალიზაცია

დაეყრდნობით შემდეგ 3 პროექტს

* [@w5/mdt](https://www.npmjs.com/package/@w5/mdt)

  სუფიქსი არის `.mdt` , შეგიძლიათ გამოიყენოთ `<+ ./coffee_plus/import.js>` ის მსგავსი სინტაქსი გარე ფაილების მითითებისთვის და `.md` სუფიქსით მარკდაუს გენერირება.

* [@w5/trmd](https://www.npmjs.com/package/@w5/trmd)

  Markdown-ის თარგმანი არ თარგმნის კოდებსა და ბმულებს და შეინახავს ნათარგმნ წინადადებებს. თუ თარგმანი შეცვლილია, მაგრამ ორიგინალი ტექსტი არ არის შეცვლილი, მისი ხელახლა შესრულება არ გადაწერს თარგმანის მოდიფიკაციას.

* [@w5/i18n](https://www.npmjs.com/package/@w5/i18n)

  ენის ფაილები `yaml` გენერირებული ვებსაიტების თარგმნისთვის.
