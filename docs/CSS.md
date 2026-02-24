# Шпаргалка по CSS

## 1. Селектори

```css
* { }                     /* Всі елементи */
div { }                   /* За тегом */
.class-name { }           /* За класом */
#id-name { }              /* За ID */
div p { }                 /* Вкладеність (всі p всередині div) */
div > p { }               /* Безпосередній нащадок */
a:hover { }               /* Стан при наведенні */
input:focus { }           /* Стан у фокусі */
```

## 2. CSS Змінні (Variables)

```css
:root {
  --main-bg-color: #f0f0f0;
  --main-text-color: #333;
  --padding-standard: 15px;
}

body {
  background-color: var(--main-bg-color);
  color: var(--main-text-color);
  padding: var(--padding-standard);
}
```

## 3. Блокова модель (Box Model)

```css
.box {
  width: 100px;           /* Ширина */
  height: 100px;          /* Висота */
  padding: 10px;          /* Внутрішній відступ */
  margin: 20px;           /* Зовнішній відступ */
  border: 1px solid #000; /* Рамка (товщина, стиль, колір) */
  box-sizing: border-box; /* Розмір враховує padding та border */
}
```

## 4. Display та видимість

```css
.block {
  display: block;         /* Блоковий елемент (займає весь рядок) */
  display: inline;        /* Інлайновий елемент (займає тільки місце для контенту) */
  display: inline-block;  /* Комбінація: займає місце, але можна задати ширину/висоту */
  display: none;          /* Приховати елемент (займає 0 місця) */
  display: grid;          /* CSS Grid */
  visibility: hidden;     /* Приховати, але займає місце */
}

.overflow {
  overflow: visible;      /* Контент виходить за межі (за замовчуванням) */
  overflow: hidden;       /* Приховати контент, що виходить за межі */
  overflow: scroll;       /* Завжди показати скролбари */
  overflow: auto;         /* Скролбари тільки якщо потрібні */
  overflow-x: auto;       /* Скролювання тільки по горизонталі */
  overflow-y: auto;       /* Скролювання тільки по вертикалі */
}
```

## 5. Текст та шрифти

```css
.text {
  font-family: Arial, sans-serif;
  font-size: 16px;
  font-weight: bold;      /* Жирність (або 700) */
  line-height: 1.5;       /* Міжрядковий інтервал */
  text-align: center;     /* Вирівнювання: left, right, center, justify */
  text-decoration: none;  /* Прибрати підкреслення (для посилань) */
  color: #2ecc71;         /* Колір тексту */
  text-transform: uppercase; /* Всі великі літери */
}
```

## 6. Flexbox (Layout)

```css
.container {
  display: flex;
  
  /* flex-direction: row | row-reverse | column | column-reverse */
  flex-direction: row;    /* Напрямок: рядок слліва направо */
  
  /* justify-content: flex-start | flex-end | center | space-between | space-around | space-evenly */
  justify-content: center; /* Вирівнювання по головній осі */
  
  /* align-items: flex-start | flex-end | center | stretch | baseline */
  align-items: center;    /* Вирівнювання по поперечній осі */
  
  /* flex-wrap: nowrap | wrap | wrap-reverse */
  flex-wrap: wrap;        /* Перенос елементів на новий рядок */
  
  gap: 10px;              /* Відстань між елементами */
}

.item {
  /* flex-grow: кількість одиниць розтягування */
  flex-grow: 1;           /* Коефіцієнт розтягування */
  
  /* flex-shrink: кількість одиниць стискання */
  flex-shrink: 0;         /* Заборона стискання */
  
  /* flex-basis: розмір до розтягування/стискання */
  flex-basis: auto;       /* Початковий розмір */
}
```

## 7. Позиціювання (Positioning)

```css
.pos {
  position: relative;     /* Відносно свого місця */
  position: absolute;     /* Відносно найближчого батька з позицією */
  position: fixed;        /* Відносно вікна браузера */
  position: sticky;       /* "Прилипає" при прокрутці */
  top: 0;
  left: 50%;
  z-index: 10;            /* Шар (чим вище значення, тим ближче до користувача) */
}
```

## 8. Фон та ефекти

```css
.visuals {
  background-image: url('image.jpg');
  background-size: cover; /* Заповнити весь блок */
  background-position: center;
  border-radius: 8px;     /* Закруглення кутів */
  box-shadow: 2px 2px 10px rgba(0,0,0,0.1); /* Тінь */
  opacity: 0.8;           /* Прозорість (0.0 - 1.0) */
  cursor: pointer;        /* Вигляд курсору (рука) */
}
```

## 9. Переходи та Анімації

```css
.animate {
  transition: all 0.3s ease-in-out; /* Плавна зміна властивостей */
}

.animate:hover {
  transform: scale(1.1);  /* Збільшення масштабу */
  transform: rotate(45deg); /* Поворот */
}
```
