# Tabs
Небольшой скрипт для работы табов.

Для его правильной работы нужно:
  1. Создать классы "hide" и "show";
  2. Настроить функцию "tabWork";
  
 Примечание: переключение информации происходит по нажатию кнопок. Т.е. при нажати на копну "1" отображается слайд #1, при нажатии на кнопку "2" отображается слайд #2 и так далее..
  
# Настройка
Для начала нужно создать два класса "hide" и "show". Они нужны для того что бы скрывать и показывать нужные объекты при необходимости. У класса "hide" должно быть свойство "display: none;", а у "show" "display: flex;". В функцию "tabWork()" мы передаем три агрумента. 

Первый -  это классы, который вы дали кнопкам для переключения (у нужных кнопах классы должны совпадать). 

    <div class="info-header-tab">BMW<</div>
    <div class="info-header-tab">Opel</div>
    <div class="info-header-tab">Lada</div>
    <div class="info-header-tab">Other</div>

Второй аргумент - это класс-обёртка в которой лежат кнопки. 

    <div class="info-header">
        <div class="info-header-tab">BMW<</div>
        <div class="info-header-tab">Opel</div>
        <div class="info-header-tab">Lada</div>
        <div class="info-header-tab">Other</div>
    </div>

Третий аргумент - это класс-обёртка ваших слайдов.

    <div class="info-tabcontent fade">
        <div class="description">
            <div class="description-title">BMW</div>
            <div class="description-text">BMW AG (German - originally an initialism for Bayerische Motoren Werke in German</div>
            <div class="description-btn">
                Check site
            </div>
        </div>
        <div class="photo">
            <img src="img/massage.jpg" alt="Massage">
        </div>
    </div>
    
Это и вся настройка. Что бы запустить скрипт, нужно его добавить в index.html (js/tabs.js) и в файле настроить под себя:     

    tabWork(".info-header-tab", ".info-header", ".info-tabcontent");
