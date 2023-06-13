# Вступительные титры из Star Wars на языках HTML, CSS
## Пример работы
![ezgif-5-0317ee7c43](https://github.com/Sazukiro/Star-Wars-Text/assets/133951840/89914f6c-acee-4469-9316-f4edcce9a4f4)
## О моей работе
В данной работе использовались два языка проргаммирования: HTML и CSS. Сама работа была выполнена в программе Visual Studio Code. Языки также взаимодействуют между собой как и в моей предыдущей работе с [карточкой и неоновой кнопкой](https://github.com/Sazukiro/Card-and-Neon-Button), но есть некоторые отличия в коде. Введённый класс `"resume"` отвечает за текст, его размеры, шрифт, цвет, оступ между букв, расстояние между строками и так далее. Самый главный парамметр в блоке `".resume"`, который как раз и придаёт такой эффект тексту - это `"perspective"`. Благодаря этому парраметру можно изменить перспективу тексту(т.е. угол обзора), достигнув того, что текст отображается как бы под углом от наблюдателя.
```cpp
.resume{
    display: flex;
    justify-content: center;
    position: relative;
    height: 800px;
    color:#feda4a;
    font-family:'Gill Sans', 'Gill Sans MT', Calibri, 'Trebuchet MS', sans-serif;
    font-size: 500%;
    font-weight: 600;
    letter-spacing: 6px;
    line-height: 150%;
  
    perspective: 400px;
  
    text-align: justify;
}
```
