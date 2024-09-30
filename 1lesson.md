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
  fetch('https://fakestoreapi.com/products')
    .then(res => res.json())
    .then(products => {
        const productsLowCost = products.filter(product => product.price < 20);
        console.log(productsLowCost);
    });
  
- 2 Вывести все категории
