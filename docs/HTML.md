# Шпаргалка по HTML

## 1. Базова структура документу

```html
<!DOCTYPE html>
<html lang="uk">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Назва сторінки</title>
  <link rel="stylesheet" href="style.css">
</head>
<body>
  <!-- Вміст сторінки -->
</body>
</html>
```

## 2. Семантичні теги структури

```html
<!-- Шапка сайту -->
<header>
  <h1>Назва сайту</h1>
  <nav>
    <a href="/">Головна</a>
    <a href="/about">Про нас</a>
    <a href="/contact">Контакти</a>
  </nav>
</header>

<!-- Основний вміст -->
<main>
  <!-- Стаття/розділ -->
  <article>
    <h2>Заголовок статті</h2>
    <p>Текст статті...</p>
  </article>

  <!-- Розділ з пов'язаним змістом -->
  <section>
    <h2>Розділ</h2>
    <p>Вміст розділу...</p>
  </section>
</main>

<!-- Бічна панель з додатковою інформацією -->
<aside>
  <h3>Корисні посилання</h3>
  <ul>
    <li><a href="#">Посилання 1</a></li>
    <li><a href="#">Посилання 2</a></li>
  </ul>
</aside>

<!-- Підвал сайту -->
<footer>
  <p>&copy; 2026 Всі права захищені</p>
</footer>
```

## 3. Контейнери (div та span)

```html
<!-- DIV - блоковий контейнер (займає весь рядок) -->
<div class="container">
  <div class="row">
    <div class="column">Колонка 1</div>
    <div class="column">Колонка 2</div>
    <div class="column">Колонка 3</div>
  </div>
</div>

<!-- SPAN - рядковий контейнер (займає тільки необхідно місце) -->
<p>Це звичайний текст з <span class="highlight">виділеним словом</span> у середині.</p>

<!-- Використання для стилізації -->
<div class="card">
  <div class="card-header">Заголовок картки</div>
  <div class="card-body">
    <p>Вміст картки</p>
  </div>
  <div class="card-footer">Підвал картки</div>
</div>

<!-- Обгортання для макету -->
<div class="flex-container">
  <div class="flex-item">Елемент 1</div>
  <div class="flex-item">Елемент 2</div>
  <div class="flex-item">Елемент 3</div>
</div>

<!-- Вбудований стиль for span -->
<p>Ціна: <span style="color: red; font-weight: bold;">₴100</span></p>
```

## 4. Заголовки та текст

```html
<h1>Заголовок 1 рівня (один на сторінці)</h1>
<h2>Заголовок 2 рівня</h2>
<h3>Заголовок 3 рівня</h3>
<h4>Заголовок 4 рівня</h4>
<h5>Заголовок 5 рівня</h5>
<h6>Заголовок 6 рівня</h6>

<p>Звичайний абзац тексту</p>

<!-- Форматування тексту -->
<strong>Жирний текст (важливий)</strong>
<em>Курсивний текст (наголос)</em>
<b>Жирний текст (без семантики)</b>
<i>Курсивний текст (без семантики)</i>
<u>Підкреслений текст</u>
<mark>Виділений текст</mark>
<del>Видалений текст</del>
<ins>Вставлений текст</ins>
<sub>Підрядковий текст</sub>
<sup>Надрядковий текст</sup>

<!-- Блоцитати та код -->
<blockquote>
  <p>Цитата з джерела</p>
  <footer>— Автор</footer>
</blockquote>

<code>inline код</code>
<pre><code>Багаторядковий код
з збереженням форматування</code></pre>
```

## 5. Списки

```html
<!-- Невпорядкований список -->
<ul>
  <li>Перший пункт</li>
  <li>Другий пункт</li>
  <li>Третій пункт</li>
</ul>

<!-- Впорядкований список -->
<ol>
  <li>Перший крок</li>
  <li>Другий крок</li>
  <li>Третій крок</li>
</ol>

<!-- Список визначень -->
<dl>
  <dt>HTML</dt>
  <dd>Мова розмітки гіпертексту</dd>
  
  <dt>CSS</dt>
  <dd>Каскадні таблиці стилів</dd>
</dl>

<!-- Вкладені списки -->
<ul>
  <li>Основний пункт
    <ul>
      <li>Вкладений пункт</li>
      <li>Вкладений пункт</li>
    </ul>
  </li>
</ul>
```

## 6. Посилання та зображення

```html
<!-- Посилання -->
<a href="https://example.com">Просте посилання</a>
<a href="/about">Внутрішнє посилання</a>
<a href="mailto:email@example.com">Email посилання</a>
<a href="tel:+380951234567">Телефон</a>
<a href="#section1">Посилання на якір</a>

<!-- Якір (посилання на розділ) -->
<h2 id="section1">Розділ 1</h2>

<!-- Зображення -->
<img src="image.jpg" alt="Опис зображення" width="300" height="200">

<!-- Зображення як посилання -->
<a href="https://example.com">
  <img src="logo.png" alt="Логотип">
</a>

<!-- Малюнок з підписом -->
<figure>
  <img src="photo.jpg" alt="Опис фото">
  <figcaption>Підпис до зображення</figcaption>
</figure>
```

## 7. Таблиці

```html
<table border="1">
  <!-- Заголовок таблиці -->
  <thead>
    <tr>
      <th>Заголовок 1</th>
      <th>Заголовок 2</th>
      <th>Заголовок 3</th>
    </tr>
  </thead>
  
  <!-- Тіло таблиці -->
  <tbody>
    <tr>
      <td>Дані 1</td>
      <td>Дані 2</td>
      <td>Дані 3</td>
    </tr>
    <tr>
      <td>Дані 4</td>
      <td>Дані 5</td>
      <td>Дані 6</td>
    </tr>
  </tbody>
  
  <!-- Підвал таблиці -->
  <tfoot>
    <tr>
      <td colspan="2">Усього:</td>
      <td>100</td>
    </tr>
  </tfoot>
</table>

<!-- colspan та rowspan -->
<table>
  <tr>
    <td colspan="2">Об'єднані 2 колонки</td>
    <td>Звичайна клітинка</td>
  </tr>
  <tr>
    <td rowspan="2">Об'єднані 2 рядки</td>
    <td>Клітинка</td>
    <td>Клітинка</td>
  </tr>
  <tr>
    <td>Клітинка</td>
    <td>Клітинка</td>
  </tr>
</table>
```

## 8. Форми та поля вводу

```html
<form action="/submit" method="POST">
  <!-- Текстове поле -->
  <label for="name">Ім'я:</label>
  <input type="text" id="name" name="name" placeholder="Введіть ім'я" required>
  
  <!-- Email -->
  <label for="email">Email:</label>
  <input type="email" id="email" name="email" required>
  
  <!-- Пароль -->
  <label for="password">Пароль:</label>
  <input type="password" id="password" name="password">
  
  <!-- Число -->
  <label for="age">Вік:</label>
  <input type="number" id="age" name="age" min="18" max="100">
  
  <!-- Дата -->
  <label for="date">Дата:</label>
  <input type="date" id="date" name="date">
  
  <!-- Чекбокс -->
  <input type="checkbox" id="agree" name="agree">
  <label for="agree">Я погоджуюся з умовами</label>
  
  <!-- Радіо кнопка -->
  <input type="radio" id="male" name="gender" value="male">
  <label for="male">Чоловіча</label>
  
  <input type="radio" id="female" name="gender" value="female">
  <label for="female">Жіноча</label>
  
  <!-- Випадаючий список -->
  <label for="country">Країна:</label>
  <select id="country" name="country">
    <option value="">-- Виберіть --</option>
    <option value="ua">Україна</option>
    <option value="pl">Польща</option>
    <option value="de">Німеччина</option>
  </select>
  
  <!-- Текстова область -->
  <label for="message">Повідомлення:</label>
  <textarea id="message" name="message" rows="5" cols="40"></textarea>
  
  <!-- Кнопки -->
  <button type="submit">Надіслати</button>
  <button type="reset">Очистити</button>
  <button type="button">Звичайна кнопка</button>
</form>
```

## 9. Атрибути та мета-теги

```html
<!-- Глобальні атрибути -->
<div id="unique-id" class="class1 class2" title="Підказка">
  <!-- id: унікальний ідентифікатор -->
  <!-- class: класи для стилізації (кілька через пробіл) -->
  <!-- title: спливаюча підказка -->
  <!-- data-*: користувацькі атрибути -->
  <span data-value="123" data-type="custom">Текст</span>
</div>

<!-- Мета-теги в head -->
<meta charset="UTF-8"> <!-- Кодування символів -->
<meta name="viewport" content="width=device-width, initial-scale=1.0"> <!-- Адаптивність -->
<meta name="description" content="Опис сторінки для пошукових двигунів">
<meta name="keywords" content="ключові слова, розділені комами">
<meta name="author" content="Автор">
<meta name="theme-color" content="#3498db"> <!-- Колір браузера -->
<meta property="og:title" content="Назва для соцмереж"> <!-- Open Graph -->
<meta property="og:description" content="Опис для соцмереж">
<meta property="og:image" content="image.jpg">

<!-- Favicon -->
<link rel="icon" href="favicon.ico" type="image/x-icon">

<!-- Зовнішні ресурси -->
<link rel="stylesheet" href="style.css">
<script src="script.js"></script>
```

## 10. Медіа (відео та аудіо)

```html
<!-- Аудіо -->
<audio controls>
  <source src="audio.mp3" type="audio/mpeg">
  <source src="audio.ogg" type="audio/ogg">
  Ваш браузер не підтримує аудіо елемент
</audio>

<!-- Відео -->
<video width="320" height="240" controls>
  <source src="video.mp4" type="video/mp4">
  <source src="video.ogg" type="video/ogg">
  Ваш браузер не підтримує відеоелемент
</video>

<!-- Iframe (вбудове вікно) -->
<iframe width="560" height="315" src="https://www.youtube.com/embed/dQw4w9WgXcQ" 
        title="YouTube video player" frameborder="0" 
        allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture">
</iframe>
```

## 11. Корисні теги

```html
<!-- Інформація -->
<details>
  <summary>Натисніть для розширення</summary>
  <p>Прихована інформація, що розверається</p>
</details>

<!-- Прогрес -->
<progress value="70" max="100"></progress>

<!-- Шкала вимірювання -->
<meter value="6" min="0" max="10"></meter>

<!-- Горизонтальна лінія -->
<hr>

<!-- Неважливий текст -->
<small>Маленький текст</small>

<!-- Час та дата -->
<time datetime="2026-02-24">24 лютого 2026</time>

<!-- Скорочення -->
<abbr title="Гіпертекстова мова розмітки">HTML</abbr>

<!-- Виділений пошуковий текст -->
<mark>Виділено</mark>
```

