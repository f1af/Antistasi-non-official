# Antistasi-non-official
**Antistasi-non-official** - кооперативная миссия для игры ARMA 3 (COOP/CTI/PvE), неофициальная версия. Вам предстоит возглавить партизанское движение и завоевать доверие 51% горожан. Для решения этой задачи вам доступны как прямые боевые действия (захват военных объектов и шахт), так и диверсионные воздействия (ограбление банка, уничтожение полевых командиров, подрыв вышек радиосвязи и многое другое).

> Отличия этой миссии от официальной - читайте ниже.
Официальную версию **Antistasi** можно найти тут: [http://www.a3antistasi.com](http://www.a3antistasi.com)

### Особенности миссии:
- наличие внутренней экономики у врага, которую можно подорвать своими действиями;
- боты атакуют без предупреждения, патрулирование вдоль линии фронта очень полезно;
- возможность управлять своими отрядами, как в стратегии (такого вы ещё не видели!);
- полный спектор оружия, от партизанских трусов до боевых самолётов;
- длительность игровой сессии ~2 месяца.

### Особенности неофициальной версии:
- вражеские боты лечат друг-друга (такого вы ещё не видели!);
- переделан геймплей: меньше рутины, больше боевых действий;
- миссия локализована и переведена на русский язык;
- добалвена внутриигровая документация на русском языке.

### Установка:
- выкачать этот репозиторий в каталог:
*c:\Users\\<Пользователь>\Documents\Arma 3\mpmissions*
- внутри игры выбрать:
Сетевая игра -> Браузер сервера -> Хост-сервер -> Алтис ->
**_Antistasi (Russian edition)_** -> ИГРАТЬ

### Запуск выделенного сервера:
- в своём клиенте steam выбрать:
"Библиотека -> Инструменты -> Arma 3 Server -> Установить"
- зайти в каталог **_config_** этого репозитория;
- скопировать файл **_server.Arma3Profile_** в каталог
*c:\Users\\<Пользовательr>\Documents\Arma 3 - Other Profiles\server*
- скопировать файлы **_server.bat_** и **_server.cfg_** в каталог
*d:\Steam\steamapps\common\Arma 3 Server*
- скопировать файл **_A3-Antistasi.Altis.pbo_** в каталог
*d:\Steam\steamapps\common\Arma 3 Server\mpmissions*
- запустить **_d:\Steam\steamapps\common\Arma 3 Server\server.bat_**

### Список отличий от оф. версии:
- #### Новая система повреждений
    - Полностью переписаны скрипты:
        - handledamage.sqf
        - inconsciente.sqf
        - pedirayuda.sqf
        - ayudar.sqf
    - Теперь шанс на хедшот можно задать изменив переменную _damAccumLimitConst.
    - Пока вы лежите раненый и ждёте помощи - вас могут добить.
    - После смерти, указывается причина смерти, кто подстрелил и кто добил.
    - Боты лечат союзных игроков вне зависимости от принадлежности к отряду.
    - Камера смерти ходит во круг вас, или во круг бота, который бежит лечить вас.
    - Упрощён алгоритм вызова лечения, теперь боты бегут к игроку намного быстрее.
    - Лечит самый близкий бот, вне зависимости от того, медик он или нет.
    - Если мимо-проходящий бот окажется ближе, то вызов лечения переключится на него.
- #### Боты врага могут лечить друг друга
    - Система повреждений унифицирована, работает как для союзников так и для врагов.
    - Для врагов шанс получить хедшот выше чем для союзников, почти в 3 раза.
    - Игроки могут лечить подстреленных, и те сдаются в плен (если в 10 метрах нет врагов).
    - Деньги даются как за добивание врага, так и если враг истечёт кровью спустя время.
- #### Улучшение FPS
    - Автоудаление мусора каждые 35 минут.
    - Удаление 15% жилых домов с карты и 30% домов из города "Кавалла".
    - Настройки производительности по умолчанию: минимум гражданских и т.п.
    - Уменьшено количество автомобилей в городах.
    - Ограничено количество солдат в гарнизоне до 20.
    - После рестарта, минные поля НЕ загружаются.
    - Удалена подсистема "roadDB" (влияла на поиск маршрута городского транспорта).
- #### Более динамичный геймплей
    - Арсенал открыт, теперь нет нужды собирать оружие.
    - Открыт арсенал на всех ящиках: после захвата игроки могут пополнить припасы.
    - На всех флагах добавлен пункт "управление штабом".
    - В боевое меню добавлен пункт "отказ от коммандования".
    - Вся покупаемая техника разблокирована (unlock) по умолчанию.
    - Увеличено количество денег, начисляемое игрокам.
    - После смерти, раньше у игроков вычитались деньги - теперь этого нет.
    - Увеличено время удаления трупов, чтобы их можно было лутать неспеша.
    - В меню покупки техники добавлены новые автомобили и бронетехника.
    - Добавлены солдаты ПЗРК, как в гарнизон так и в меню рекрутирования.
    - Винтовки для гарнизона берутся не случайные, а из заданного списка.
    - Гарнизон одет в нормальную форму и броню уже в начале игры.
    - Если вас спалили, кнопка "под прикрытием" будет работать снова спустя 3 минуты.
        - Если вы притворялись гражданским и вас спалили, теперь достаточно отбежать от врагов на 350 местров, и вновь нажать на кнопку "под прикрытием".
- #### Внутриигровая документация
    - При входе на сервер, игроку отображается внутриигровая документация.
    - Все пункты документации отвечают на Часто Задаваемые Вопросы.
    - Внизу диалогового окна "Справочная" есть кнопка "больше не показывать это окно".
    - Вызов "Справочная" (т.е. документация) добавлен в боевое меню и на карту в штабе.
- #### Маркер местоположения игрока
    - Полностью переписан скрипт:
        - playermarkers.sqf
    - Для отображения местоположения других игроков рация больше не нужна.
    - На карте отмечены не только другие игроки, но и сам игрок.
    - Убран баг: отображались несуществующие игроки, которые ушли с сервера нажав Alt+F4.
    - Боты вашего отряда теперь тоже отмечаются на карте, это очень удобно!
- #### Визуальные эффекты
    - Добавлен скрипт случайной погоды.
    - Добавлен скрипт снега и пара изо рта.
    - Вражеские объекты омечаются теперь красным цветом, а не зелёным.
    - Смена цвето в боевом меню.
    - Добавлен пост-эффект, повышающий контрастность изображения.
    - Новогодний логотип миссии.
- #### Администрирование
    - Добавлена отладочная консоль и режим Zeos для администратора.
    - Исправлен баг: спустя время, появлялся густой туман и мешал играть.
    - При включении RHS AF RF список вражеских юнитов остаётся прежним.
        - Русским игрокам не понравилось воевать против войск Российской Федерации, однако, очень хочется пострелять их "Колаша". Поэтому логика миссии по добавлению RHS была упразднена: при включении этого мода на сервере, только лишь в арсенали вы увидите РХС-ное оружие, и нигде больше.
    - Во время входа на сервер, первый свободный слот присваивается автоматически.
    - Разница в слотах: только медики личат до 100%, только инженеры могут чинить.
        - Раньше, разница в слотах была не только функциональная. Персонажи под различными слотами имели различные параметры "усталости", "камуфляжа" и "скрытности". Так, если одеть привычный по компании Arma3 боекомплект, то персонаж будет перегружен и не сможет бегать. У многих игроков эта фича вызывала недоумение, поэтому фича была упразднена.
    - Отключены вопросы по настройке сервера при старте и рестарте миссии.
        - Вопросы "Менять командира?", "Включить сервер-лист?", "Загрузить последнее сохранение?" - жутко надоели, потому что выбор всегда один и тот же: "нет, нет, да". Сервер-лист же можно включить в процессе игры, на карте в штабе.
    - После смерти Петерса, база автоматически переносится на изначальное место.
        - Раньше, при смерти главного коммандующего Петерса, у игрока-коммандира отображалась карта с просьбой выбрать новое рассположение штаба. Если игрок-коммандир наживает в этот момент Alt-F4, то миссия подвисает: Петерс убит, штаб не активен, а новый не поставить.
    - При старте миссии убран вопрос об установке штаба.
    - Тип игры изменён на CTI, так игрокам легче найти эту миссию.
