---
id: docs_cli_why
guide: docs_cli
layout: guide
---

<p class="lead">Показуе інформацію про те, чому встановлюєно пакет.</p>

##### `yarn why <query>` <a class="toc" id="toc-yarn-why" href="#toc-yarn-why"></a>

Ця команда визначає, чому встановлено пакет, деталізуючи, які інші пакунки від нього залежать.
Наприклад, чи було пакет явно позначено як залежність у маніфесті `package.json`.

```sh
yarn why jest
```

```
yarn why vx.x.x
[1/4] 🤔  Why do we have the module "jest"...? / Чому ми маємо модуль "jest"...?
[2/4] 🚚  Initializing dependency graph... / Ініціалізація графіку залежностей ...
[3/4] 🔍  Finding dependency... / Пошук залежностей ...
[4/4] 🚡  Calculating file sizes... / Розрахунок розміру файлу ...
info Has been hoisted to "jest" / "jest" було піднятий
info This module exists because it's specified in "devDependencies". / інформація Цей модуль існує, оскільки він вказаний у "devDependencies".
info Disk size without dependencies: "1.29kB" / Розмір диска без залежностей: "1,29 кБ"
info Disk size with unique dependencies: "101.31kB" / Розмір диска з унікальними залежностями: "101,31 кБ"
info Disk size with transitive dependencies: "20.35MB" / Розмір диска з перехідними залежностями: "20,35 МБ"
info Amount of shared dependencies: 125 / Кількість спільних залежностей: 125
```

### Аргументи запиту <a class="toc" id="toc-query-argument" href="#toc-query-argument"></a>

Обов’язковим аргументом запиту для `yarn why` може бути будь-що з:

- ім'я пакету (як у наведеному вище прикладі)
- папка розташування пакету; наприклад: `yarn why node_modules/once`
- назва файлу у папці пакета; наприклад: `yarn why node_modules/once/once.js`

Розташування файлів також можуть бути вказано абсолютними.
