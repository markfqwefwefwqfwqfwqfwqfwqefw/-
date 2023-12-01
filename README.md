<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <style>
        @keyframes changeColor {
            0% { color: red; }
            25% { color: blue; }
            50% { color: green; }
            75% { color: orange; }
            100% { color: purple; }
        }

        h1 {
            font-size: 2em;
            animation: changeColor 5s infinite; /* изменяйте продолжительность анимации по желанию */
        }
    </style>
    <title>Полина не списывай!</title>
</head>
<body>
    <h1>Полина не списывай!</h1>
</body>
</html>



 <!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Исторический тест</title>
</head>
<body>

<h1>Исторический тест</h1>

<form id="historyQuizForm">
    <ol>
        <li>
            <p>Какие годы охватывают правление Бориса Годунова?</p>
            <label><input type="radio" name="q1" value="correct"> 1598-1605</label>
            <label><input type="radio" name="q1" value="incorrect"> 1605-1610</label>
            <label><input type="radio" name="q1" value="incorrect"> 1610-1613</label>
        </li>
        <li>
            <p>Кто был на троне России после Бориса Годунова и до Лжедмитрия I?</p>
            <label><input type="radio" name="q2" value="incorrect"> Алексей Михайлович</label>
            <label><input type="radio" name="q2" value="correct"> Василий Шуйский</label>
            <label><input type="radio" name="q2" value="incorrect"> Михаил Романов</label>
        </li>
        <li>
            <p>Как завершилось правление Лжедмитрия I?</p>
            <label><input type="radio" name="q3" value="correct"> Убийство</label>
            <label><input type="radio" name="q3" value="incorrect"> Естественная смерть</label>
            <label><input type="radio" name="q3" value="incorrect"> Отречение</label>
        </li>
        <li>
            <p>Кто стал правителем России после Лжедмитрия I?</p>
            <label><input type="radio" name="q4" value="incorrect"> Василий Шуйский</label>
            <label><input type="radio" name="q4" value="correct"> Михаил Романов</label>
            <label><input type="radio" name="q4" value="incorrect"> Алексей Михайлович</label>
        </li>
        <li>
            <p>Какой князь правил Россией в период с 1606 по 1610 год?</p>
            <label><input type="radio" name="q5" value="correct"> Василий Шуйский</label>
            <label><input type="radio" name="q5" value="incorrect"> Михаил Романов</label>
            <label><input type="radio" name="q5" value="incorrect"> Алексей Михайлович</label>
        </li>
        <li>
            <p>Какое событие привело к выбору Михаила Фёдоровича на трон?</p>
            <label><input type="radio" name="q6" value="incorrect"> Смутное время</label>
            <label><input type="radio" name="q6" value="correct"> Возведение на Московский престол</label>
            <label><input type="radio" name="q6" value="incorrect"> Убийство предыдущего монарха</label>
        </li>
        <li>
            <p>Сколько лет длилось правление Алексея Михайловича?</p>
            <label><input type="radio" name="q7" value="incorrect"> 30 лет</label>
            <label><input type="radio" name="q7" value="correct"> 31 год</label>
            <label><input type="radio" name="q7" value="incorrect"> 32 года</label>
        </li>
        <li>
            <p>Кто стал правителем России после Алексея Михайловича?</p>
            <label><input type="radio" name="q8" value="correct"> Федор Алексеевич</label>
            <label><input type="radio" name="q8" value="incorrect"> Петр I</label>
            <label><input type="radio" name="q8" value="incorrect"> Екатерина II</label>
        </li>
        <li>
            <p>Как завершилось правление Софьи Алексеевны?</p>
            <label><input type="radio" name="q9" value="incorrect"> Отречение</label>
            <label><input type="radio" name="q9" value="correct"> Смещение</label>
            <label><input type="radio" name="q9" value="incorrect"> Естественная смерть</label>
        </li>
        <li>
            <p>Кто был на троне России в период с 1682 по 1696 год?</p>
            <label><input type="radio" name="q10" value="incorrect"> Петр I</label>
            <label><input type="radio" name="q10" value="correct"> Иван V</label>
            <label><input type="radio" name="q10" value="incorrect"> Екатерина I</label>
        </li>
    </ol>

    <button type="button" onclick="checkAnswers()">Проверить ответы</button>
</form>

<p id="result"></p>

<script>
    function checkAnswers() {
        // Создаем объект для хранения количества правильных и неправильных ответов
        var score = { correct: 0, incorrect: 0 };

        // Перебираем все вопросы в форме
        for (var i = 1; i <= 10; i++) {
            // Получаем выбранный ответ
            var selectedAnswer = document.querySelector('input[name="q' + i + '"]:checked');

            // Если ответ выбран и он правильный, увеличиваем счетчик правильных ответов
            if (selectedAnswer && selectedAnswer.value === "correct") {
                score.correct++;
            } else {
                // В противном случае увеличиваем счетчик неправильных ответов
                score.incorrect++;
            }
        }

        // Выводим результат
        document.getElementById("result").innerHTML = "Правильных ответов: " + score.correct +
                                                          "<br>Неправильных ответов: " + score.incorrect;
    }
</script>

</body>
</html>
# -
