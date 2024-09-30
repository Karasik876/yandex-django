## Задание:
```
REST API Fake Store - https://fakestoreapi.com/

Самостоятельно:
1 Вывести продукты, цена которых <20
2 Вывести все категории
3 Вывести все продукты с категорией  "jewelery"
4 Вывести всех пользователей
5 Добавить пользователя со своим именем.
```

***

- 1 Вывести продукты, цена которых <20
  ```
  fetch('https://fakestoreapi.com/products')
    .then(res => res.json())
    .then(products => {
        const productsLowCost = products.filter(product => product.price < 20);
        console.log(productsLowCost);
    });
  ```
- 2 Вывести все категории
  ```
  fetch('https://fakestoreapi.com/products/categories')
    .then(res => res.json())
    .then(categories => console.log(categories));
  ```
- 3 Вывести все продукты с категорией  "jewelery"
  ```
  fetch('https://fakestoreapi.com/products/category/jewelery')
    .then(res => res.json())
    .then(jeweleryProducts => console.log(jeweleryProducts));
  ```
- 4 Вывести всех пользователей
  ```
  fetch('https://fakestoreapi.com/users')
    .then(res => res.json())
    .then(users => console.log(users));
  ```
- 5 Добавить пользователя со своим именем
```
  fetch('https://fakestoreapi.com/users', {
    method: "POST",
    body: JSON.stringify({
        email: 'Kapustaa11@yandex.ru',
        username: 'Karasik123',
        password: 'qwertyuiop123456789',
        name: {
            firstname: 'Ilya',
            lastname: 'Krutikov'
        },
        address: {
            city: 'Ekaterinburg',
            street: 'Lenina st.',
            number: 11,
            zipcode: '98765-1024',
            geolocation: {
                lat: '30.24788',
                long: '-20.545419'
            }
        },
        phone: '123-456-7890'
    }),
    headers: {
        'Content-Type': 'application/json'
    }
})
    .then(res => res.json())
    .then(newUser => console.log(newUser));
```
