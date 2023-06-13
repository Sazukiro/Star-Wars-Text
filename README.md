# Вступительные титры из Star Wars на языках HTML, CSS
## Пример работы
![ezgif-5-0317ee7c43](https://github.com/Sazukiro/Star-Wars-Text/assets/133951840/89914f6c-acee-4469-9316-f4edcce9a4f4)
## О моей работе
В данной работе использовались два языка проргаммирования: HTML и CSS. Сама работа была выполнена в программе Visual Studio Code. Языки также взаимодействуют между собой как и в моей предыдущей работе с [карточкой и неоновой кнопкой](https://github.com/Sazukiro/Card-and-Neon-Button), но есть некоторые отличия в коде. Введённый класс `"resume"` отвечает за текст, его размеры, шрифт, цвет, оступ между букв, расстояние между строками и так далее. Самый главный парамметр в блоке `".resume"`, который как раз и придаёт такой эффект тексту - это `"perspective"`. Благодаря этому парраметру можно изменить перспективу тексту(т.е. угол обзора), достигнув того, что текст отображается как бы под углом от наблюдателя.
```css
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
Класс `"crawl"` же отвечает за перемещение данного текста вверх. В блоке `".crawl"` в парамметрах `"animation"` и `"-webkit-animation"` определяется скорость анимации и её вид, также указывается то, что она идёт по прямой. В свойстве `"transform-origin"` указывается с какой точки отображаемого объекта будут применятся преобразования В моём случае данная точка или источник находится по-середине относительно `оси X` и внизу относительно `оси Y` (X = 50%, Y = 100%). Также данный источник может служить центром вращения для свойства `"rotate()"`.

```css
.crawl{
    position: relative;
    top: 9999px;
    transform-origin: 50% 100% ;
    animation: crawl 60s linear ;
    -webkit-animation: crawl 60s linear ;
}
```
Правило `@keyframes` устанавливает ключевые кадры при анимации элемента. В данной работе это правило применяется к классу `"crawl"` и ключевыми кадрами являются начальные и конечные свойства объекта такие как положение (`top 0px` -> `top -6000px`), угл наклона и многие другие, а процентами `0%` и `100%` обозначаются начальный и конечный кадр.

Для того чтобы достичь ещё большей схожести с оригиналом применяем такие свойства как: `transform`, `-webkit-transform`, `-moz-transform`, `-ms-transform`, `-o-transform`. Благодаря ним текст осуществляет небольшой поворот.

```css
@keyframes crawl{
    0%{
        top: 0px;
        transform: rotatex(20deg) translateZ(0);
        -webkit-transform: rotatex(20deg) translateZ(0);
        -moz-transform: rotatex(20deg) translateZ(0);
        -ms-transform: rotatex(20deg) translateZ(0);
        -o-transform: rotatex(20deg) translateZ(0);
}
    100%{
        top: -6000px;
        transform: rotatex(25deg) translateZ(-2500px);
        -webkit-transform: rotatex(25deg) translateZ(-2500px);
        -moz-transform: rotatex(25deg) translateZ(-2500px);
        -ms-transform: rotatex(25deg) translateZ(-2500px);
        -o-transform: rotatex(25deg) translateZ(-2500px);
}
```
