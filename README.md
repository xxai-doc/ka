<p align="center"><a href="https://xxai.art"><img src="https://cdn.jsdelivr.net/gh/xxai-art/doc/logo.svg"/></a><br/><a href="https://xxai.art"><img src="https://cdn.jsdelivr.net/gh/xxai-art/doc/xxai.svg"/></a></p><p align="center"><a href="https://github.com/xxai-art/doc#readme"><img alt="I18N" src="https://cdn.jsdelivr.net/gh/wactax/img/t.svg"/></a>　<a href="https://groups.google.com/u/0/g/xxai-art"><img alt="Google Groups" src="https://cdn.jsdelivr.net/gh/wactax/img/g-groups.svg"/></a></p>

რეკომენდირებულია დააინსტალიროთ ჯერ nodejs, [direnv](https://direnv.net) , [bun](https://github.com/oven-sh/bun) და შემდეგ `direnv allow` დირექტორიაში შესვლის შემდეგ ( [.envrc](https://github.com/xxai-art/doc/blob/main/.envrc) შესრულდება ავტომატურად დირექტორიაში შესვლის შემდეგ).

მნიშვნელობა არის: ჩინური თარგმანი იაპონურად, კორეული, ინგლისური, ინგლისური თარგმანი ყველა სხვა ენაზე. თუ გსურთ მხოლოდ ჩინური და ინგლისური ენის მხარდაჭერა, შეგიძლიათ უბრალოდ დაწეროთ `zh: en` .

მნიშვნელობა არის: ჩინური თარგმანი იაპონურად, კორეული, ინგლისური, ინგლისური თარგმანი ყველა სხვა ენაზე. თუ გსურთ მხოლოდ ჩინური და ინგლისური ენის მხარდაჭერა, შეგიძლიათ უბრალოდ დაწეროთ `zh: en` .

* [წინა ბოლო კოდი](https://github.com/xxai-art/web)
* [ენების პაკეტები მთლიანად საიტისთვის](https://github.com/xxai-art/web/tree/main/i18n)
* [ენის პაკეტები შესვლის მოდულებისთვის](https://github.com/wacpkg/user/tree/main/ui.i18n)
* [ვებსაიტის მრავალენოვანი დოკუმენტაცია](https://github.com/xxai-doc)

ფრონტალური პროგრამირების ენაა [@w5/coffee_plus](http://npmjs.com/@w5/coffee_plus) , რომელიც ამატებს ზოგიერთ ფუნქციას coffeescript სინტაქსის საფუძველზე, იხილეთ [./coffee_plus.md](./coffee_plus.md) .

## ვებსაიტების და დოკუმენტების ინტერნაციონალიზაცია

დაეყრდნობით შემდეგ 3 პროექტს

* [@w5/mdt](https://www.npmjs.com/package/@w5/mdt)

  სუფიქსი არის `.mdt` , შეგიძლიათ გამოიყენოთ `<+ ./coffee_plus/import.js>` ის მსგავსი სინტაქსი გარე ფაილების მითითებისთვის და `.md` სუფიქსით მარკდაუს გენერირება.

* [@w5/trmd](https://www.npmjs.com/package/@w5/trmd)

  Markdown-ის თარგმანი არ თარგმნის კოდებსა და ბმულებს და შეინახავს ნათარგმნ წინადადებებს. თუ თარგმანი შეცვლილია, მაგრამ ორიგინალი ტექსტი არ არის შეცვლილი, მისი ხელახლა შესრულება არ გადაწერს თარგმანის მოდიფიკაციას.

* [@w5/i18n](https://www.npmjs.com/package/@w5/i18n)

  ენის ფაილები `yaml` გენერირებული ვებსაიტების თარგმნისთვის.

### დოკუმენტის თარგმანის ავტომატიზაციის ინსტრუქციები

იხილეთ კოდის საცავი [xxai-art/doc](https://github.com/xxai-art/doc)

რეკომენდირებულია დააინსტალიროთ ჯერ nodejs, [direnv](https://direnv.net) , [bun](https://github.com/oven-sh/bun) და შემდეგ `direnv allow` დირექტორიაში შესვლის შემდეგ ( [.envrc](https://github.com/xxai-art/doc/blob/main/.envrc) შესრულდება ავტომატურად დირექტორიაში შესვლის შემდეგ).

იმისათვის, რომ თავიდან ავიცილოთ ასობით ენაზე თარგმნილი დიდი კოდის ბაზა, მე შევქმენი ცალკე კოდის ბაზა თითოეული ენისთვის და შევქმენი ორგანიზაცია კოდის ბაზის შესანახად.

გარემოს ცვლადის `GITHUB_ACCESS_TOKEN` დაყენება და შემდეგ [create.github.coffee-ის](https://github.com/xxai-art/doc/blob/main/create.github.coffee) გაშვება ავტომატურად შექმნის კოდის საცავს.

რა თქმა უნდა, თქვენ ასევე შეგიძლიათ განათავსოთ ის კოდის ბაზაში.

თარგმანის სკრიპტის მითითება [run.sh](https://github.com/xxai-art/doc/blob/main/run.sh)

სკრიპტის კოდი ინტერპრეტირებულია შემდეგნაირად:

[bux](https://bun.sh/docs/cli/bunx) არის npx-ის ჩანაცვლება, რაც უფრო სწრაფია. რა თქმა უნდა, თუ არ გაქვთ დაინსტალირებული bun, ამის ნაცვლად შეგიძლიათ გამოიყენოთ `npx` .

`bunx mdt zh` ასახავს `.mdt` zh დირექტორიაში როგორც `.md` , იხილეთ 2 დაკავშირებული ფაილი ქვემოთ

* [coffee_plus.mdt](https://github.com/xxai-doc/zh/blob/main/coffee_plus.mdt)
* [coffee_plus.md](https://github.com/xxai-doc/zh/blob/main/coffee_plus.md)

`bunx i18n` არის თარგმანის ძირითადი კოდი (თუ თქვენ გაქვთ დაინსტალირებული მხოლოდ `nodejs` , მაგრამ `bun` და `direnv` არ არის დაინსტალირებული, შეგიძლიათ ასევე გაუშვათ `npx i18n` თარგმნისთვის).

ის გააანალიზებს [i18n.yml-ს](https://github.com/xxai-art/doc/blob/main/i18n.yml) , `i18n.yml` ის კონფიგურაცია ამ დოკუმენტში შემდეგია:

```
en:
zh: ja ko en
```

მნიშვნელობა არის: ჩინური თარგმანი იაპონურად, კორეული, ინგლისური, ინგლისური თარგმანი ყველა სხვა ენაზე. თუ გსურთ მხოლოდ ჩინური და ინგლისური ენის მხარდაჭერა, შეგიძლიათ უბრალოდ დაწეროთ `zh: en` .

ბოლო არის [gen.README.coffee](https://github.com/xxai-art/doc/blob/main/gen.README.coffee) , რომელიც ამოიღებს შინაარსს მთავარ სათაურსა და თითოეული ენის `README.md` ის პირველ ქვესათაურს შორის, რათა შექმნას ჩანაწერი `README.md` . კოდი ძალიან მარტივია, შეგიძლიათ თავად ნახოთ.

Google API გამოიყენება უფასო თარგმნისთვის. თუ Google-ზე წვდომა არ გაქვთ, გთხოვთ, დააკონფიგურიროთ და დააყენოთ პროქსი, როგორიცაა:

```
export https_proxy=http://127.0.0.1:7890 http_proxy=http://127.0.0.1:7890 all_proxy=socks5://127.0.0.1:7890
```

თარგმანის სკრიპტი წარმოქმნის თარგმნილ ქეშს `.i18n` დირექტორიაში, გთხოვთ, შეამოწმოთ იგი `git status` და დაამატოთ კოდის საცავში, რათა თავიდან აიცილოთ განმეორებითი თარგმანები.

გთხოვთ, გაუშვით `bunx i18n` ყოველ ჯერზე, როცა შეცვლით თარგმანს ქეშის განახლებისთვის.

თუ ორიგინალი ტექსტი და თარგმანი ერთდროულად შეცვლილია, ქეში აირევა, ასე რომ, თუ შეცვლა გსურთ, შეგიძლიათ მხოლოდ ერთი შეცვალოთ და შემდეგ გაუშვით `bunx i18n` ქეშის განახლებისთვის.
