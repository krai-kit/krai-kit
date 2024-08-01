# {{ NgDocPage.title }}

Повідомлення використовуються для відображення вбудованих сповіщень. Вони допомагають користувачам швидко отримувати важливу інформацію або попередження під час взаємодії з додатком.

### API

Посилання на **API** - `AlertComponent`

### Імпорт

```ts
import { AlertComponent } from '@krai-tech/kit/alert';
```

### Типи

`AlertComponent` підтримує кілька типів сповіщень, кожен з яких має своє призначення та вигляд.

#### За замовчуванням

Використовується для відображення звичайних повідомлень без особливого стилістичного акценту. Це сповіщення не має спеціального значення і підходить для загальних інформаційних повідомлень.

```html name="alert.component.ts"
<kri-alert>alert message</kri-alert>
```

{{ NgDocActions.demo("AlertDemoComponent", { container: false, inputs: {text: "Дбайливо все спакуємо в обрані торбинки. Але, якщо їх буде замало, додамо фірмові пакети «Сільпо»."} }) }}

#### Інформаційне

Використовується для відображення інформаційних повідомлень, що мають значення для користувача. Цей тип сповіщень забезпечує користувачів корисною інформацією.

```html name="alert.component.ts"
<kri-alert type="info">alert message</kri-alert>
```

{{ NgDocActions.demo("AlertDemoComponent", { container: false, inputs: {type: "info", text: "Дбайливо все спакуємо в обрані торбинки. Але, якщо їх буде замало, додамо фірмові пакети «Сільпо»."} }) }}

#### Успіх

Використовується для повідомлень про успішне виконання дій або операцій. Цей тип сповіщень інформує користувачів про те, що все пройшло вдало.

```html name="alert.component.ts"
<kri-alert type="success">alert message</kri-alert>
```

{{ NgDocActions.demo("AlertDemoComponent", { container: false, inputs: {type: "success", text: "Збирання вашого замовлення в <strong>фірмові пакети «Сільпо»</strong> успішне!"} }) }}

#### Попередження

Використовується для відображення попереджень про можливі проблеми або необхідність уваги. Цей тип сповіщень звертає увагу користувачів на важливі деталі або потенційні проблеми.

```html name="alert.component.ts"
<kri-alert type="warning">alert message</kri-alert>
```

{{ NgDocActions.demo("AlertDemoComponent", { container: false, inputs: {type: "warning", text: "Вартість товарів на вагу може трішки змінитися після збирання. Дяка за розуміння! 🧡 "} }) }}

#### Небезпека

Використовується для відображення критичних попереджень про помилки або небезпечні ситуації. Цей тип сповіщень допомагає користувачам уникати серйозних проблем або помилок.

```html name="alert.component.ts"
<kri-alert type="danger">alert message</kri-alert>
```

{{ NgDocActions.demo("AlertDemoComponent", { container: false, inputs: {type: "danger", text: "<strong>Овва, надто важко.</strong> <br> Знаємо, кортить всього й одразу. 😳 Але можемо доставити не більше 30 кг."} }) }}

### Змінити іконку

Сповіщення також підтримують зміну іконки для більшої гнучкості та інформативності. Це дозволяє використовувати спеціальні іконки `IconComponent` для певних типів сповіщень, що робить їх більш виразними та зрозумілими.

```html name="alert.component.ts"
<kri-alert type="danger" icon="products" [iconColor]="#DA291C">alert message</kri-alert>
```

{{ NgDocActions.demo("AlertDemoComponent", { container: false, inputs: {type: "danger", icon: "products", iconColor: "#DA291C", text: "<strong>Овва, надто важко.</strong> <br> Знаємо, кортить всього й одразу. 😳 Але можемо доставити не більше 30 кг."} }) }}

### Закрити алерт

Для сповіщень, що потребують можливості закриття користувачем, можна додати кнопку закриття. Це зручно для користувачів, оскільки вони можуть самостійно закрити сповіщення після ознайомлення з інформацією.

```html name="alert.component.ts"
<kri-alert type="info" [showCloseBtn]="true" (closeAlert)="myFunction($event)">alert message</kri-alert>
```

{{ NgDocActions.demo("AlertDemoComponent", { container: false, inputs: {type: "info", showCloseBtn: true, text: "Дбайливо все спакуємо в обрані торбинки. Але, якщо їх буде замало, додамо фірмові пакети «Сільпо»."} }) }}

### Пісочниця

Цей розділ дозволяє взаємодіяти з різними варіантами алертів та налаштовувати їх параметри у реальному часі, щоб побачити, як вони будуть виглядати та поводитися в інтерфейсі.

{{ NgDocActions.playground("AlertPlayground") }}
