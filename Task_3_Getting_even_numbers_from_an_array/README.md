# TASK_3

- [x] Маєте масив чисел. Використовуйте вже існуючі методи масиву для створення нового масиву, в якому лише парні числа з оригінального масиву.

## Filter

>Метод `filter` використовується для створення нового масиву, що містить елементи початкового масиву, які задовольняють певну умову. У нашому випадку, ми фільтруємо парні числа.

```javascript
const newMassFilters = mass.filter(number => number % 2 === 0);
console.log(newMassFilters); // [4, 6, 8, 2, 8, 2]
```
## Map

>Метод map застосовує задану функцію до кожного елемента масиву і створює новий масив з результатами. Ми використовуємо його для відфільтрування парних чисел, але результатом є масив, який може містити undefined, тому ми застосовуємо filter, щоб видалити ці значення.

````javascript
const newMassMap = mass.map(number => {
    if (number % 2 === 0) {
        return number;
    }
});
console.log(newMassMap.filter(element => element !== undefined)); // [4, 6, 8, 2, 8, 2]
````

# Reduce

>Метод reduce використовується для зведення масиву до одного значення. У нашому випадку, ми використовуємо його для створення нового масиву, який містить парні числа.



````javascript
const newMassReduce = mass.reduce((accumulator, currentValue) => {
    if (currentValue % 2 === 0) {
        accumulator.push(currentValue);
    }
    return accumulator;
}, []);
console.log(newMassReduce); // [4, 6, 8, 2, 8, 2]

````

## forEach

>Метод forEach використовується для ітерації по кожному елементу масиву та виконання певних операцій. Ми використовуємо його для фільтрації парних чисел.

````javascript
const newMassFind = [];
mass.forEach(number => {
    if (number % 2 === 0) {
        newMassFind.push(number);
    }
});
console.log(newMassFind); // [4, 6, 8, 2, 8, 2]
````