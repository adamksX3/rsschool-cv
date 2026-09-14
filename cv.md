# Кирилл Адамчик

## Обо мне

Мне 23 года, работаю в логистическом центре, в свободное время самостоятельно изучаю программирование. Начал с Python, затем перешёл к JavaScript и базовой вёрстке — сейчас больше интересует фронтенд-разработка, а не чистый бэкенд. Прохожу курс RS School, чтобы структурировать знания и двигаться дальше в профессию разработчика. В планах изучить один из фрейморков и "пощупать" TypeScript. По факту считаю себя новичком, знаю немного базы.

## Контакты

- TG: [@S3akiraXlll](https://t.me/S3akiraXlll)
- Email: [aga.dadaon@mail.ru](mailto:aga.dadaon@mail.ru)
- Discord: hatemyego
- GitHub: [adamksX3](https://github.com/adamksX3)

## Навыки

- JavaScript
- Python
- HTML
- CSS
- Git
- GitHub

## Пример кода

Фрагмент из мини-проекта интернет-магазина — расчёт цены со скидкой и добавление товара в корзину с проверкой наличия на складе:

```js
const products = [
  { id: 1, name: "iPhone 16", price: 999, discount: 10, stock: 5 },
  { id: 2, name: "MacBook Air", price: 1299, discount: 5, stock: 4 },
  { id: 3, name: "AirPods Pro", price: 249, discount: 20, stock: 8 }
];

let cart = [];

const getFinalPrice = product => {
  return product.price * (1 - product.discount / 100);
};

const addToCart = (product, quantity = 1) => {
  if (!product || product.stock === 0) {
    console.log("Товар недоступен");
    return;
  }

  if (quantity > product.stock) {
    console.log(`На складе только ${product.stock} шт.`);
    return;
  }

  const existingProduct = cart.find(item => item.product.id === product.id);

  if (existingProduct) {
    existingProduct.quantity += quantity;
  } else {
    cart.push({ product, quantity });
  }

  console.log(`${product.name} добавлен в корзину`);
};

const getCartTotal = () => {
  return cart.reduce((total, item) => {
    const price = getFinalPrice(item.product);
    return total + price * item.quantity;
  }, 0);
};
```

## Опыт работы

Коммерческого опыта в разработке пока нет — я в процессе перехода в профессию. Писал пару пет-проектов для практики. В основном на чистом JS без использования фреймворков. Верстал односоставные странички для сайта и в целом-то не углублялся в стилизацию, т.к. пытался делать упор на сам язык.


## Образование

- БГУ — 2 курса (не окончено)
- Stepik — курсы по Python
- Курсы и учебник — JavaScript
- YouTube — вёрстка на HTML и CSS, Figma.

## Английский язык

Уровень B1.
