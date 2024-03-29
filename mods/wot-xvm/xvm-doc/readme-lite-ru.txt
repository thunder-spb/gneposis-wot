﻿Оглавление:
  1. Общая информация
  2. Установка
  3. Обновление
  4. Дополнительная информация по конфигурационному файлу

-----------------------------------------------------------
1. ОБЩАЯ ИНФОРМАЦИЯ
-----------------------------------------------------------

  Этот мод включает в себя следующие возможности:
    * Маркеры над танками (бывший OverTargetMarkers)
    * Отключение посмертной панели
    * Управление зеркалированием иконок
    * Управление "ушами" (ширина, прозрачность, содержание)
    * Часы на экране загрузки боя
    * Иконки игрока/клана
    * Разные наборы иконок техники
    * Рейтинг игроков в игре (только в пакете xvm-full)

  Сайт проекта: http://code.google.com/p/wot-xvm/
  Поддержка:    http://forum.bulychev.net/viewforum.php?f=6
  FAQ:          http://www.koreanrandom.com/forum/topic/1381-faq-otveti-na-chastie-voprosi-po-xvm/
  Редактор:     https://sites.google.com/site/sirmaxwiki/xvm-editor

-----------------------------------------------------------
2. УСТАНОВКА
-----------------------------------------------------------

  1. Разархивировать архив в папку с игрой:
     Правой кнопкой на архив -> "Извлечь все..." -> выбрать папку игры -> "Извлечь"

  2. По умолчанию ничего настраивать не надо.

     Если нужны не стандартные настройки, необходимо создать конфигурационный файл:
       \res_mods\<game version>\gui\flash\XVM.xvmconf

     Можно скопировать готовый из папки \xvm-doc\samples\, или воспользоваться
     онлайн-редактором: https://sites.google.com/site/sirmaxwiki/xvm-editor

     Старые конфигурационные файлы OTMData.xml тоже поддерживаются, вы можете
     их использовать если вам не нужны новые возможности.

     Все возможные настройки можно посмотреть в этом файле:
       \xvm-doc\samples\Lite config RU\XVM.xvmconf

     Внимание: Если вы меняете конфиг вручную, используйте Блокнот (notepad),
     НЕ используйте word, wordpad и подобные редакторы)

-----------------------------------------------------------
3. ОБНОВЛЕНИЕ
-----------------------------------------------------------

  1. Разархивировать архив в папку с игрой:
     Правой кнопкой на архив -> "Извлечь все..." -> выбрать папку игры -> "Извлечь"

  2. Если произошло обновление версии игры, скопируйте ваш конфиг:
     из res_mods/[СТАРАЯ ВЕРСИЯ]/gui/flash/XVM.xvmconf
     в res_mods/[НОВАЯ ВЕРСИЯ]/gui/flash/XVM.xvmconf

  3. Больше НИЧЕГО делать НЕ НАДО.

-----------------------------------------------------------
4. ДОПОЛНИТЕЛЬНАЯ ИНФОРМАЦИЯ ПО КОНФИГУРАЦИОННОМУ ФАЙЛУ
-----------------------------------------------------------

  Конфигурационный файл мода:
    \res_mods\<game version>\gui\flash\XVM.xvmconf
  Можно скопировать готовый конфиг из папки \xvm-doc\samples\
  Можно создать новый конфиг или изменить существующий с помощью онлайн-редактора:
    https://sites.google.com/site/sirmaxwiki/xvm-editor

  Все возможные параметры конфига можно посмотреть в конфиге с русскими комментариями,
  который находится в папке документации в архиве мода:
    \xvm-doc\samples\Lite config RU\XVM.xvmconf

  Используемые макросы:
    В ушах:
      {{nick}}       - ник игрока
      {{vehicle}}    - название танка

    В маркерах над танком:
      {{hp}}         - текущее здоровье
      {{hp-ratio}}   - процент текущего здоровья (без символа '%')
      {{hp-max}}     - максимальное здоровье
      {{nick}}       - ник игрока
      {{vehicle}}    - название танка
      {{level}}      - уровень танка арабскими цифрами
      {{dmg}}        - количество отнятого здоровья
      {{dmg-ratio}}  - процент отнятого здоровья (без символа '%')

    Макросы динамического цвета:
      {{c:hp}}       - цвет в зависимости от текущего здоровья (только в маркерах)
      {{c:hp-ratio}} - цвет в зависимости от процента текущего здоровья (только в маркерах)

    Макросы динамической прозрачности:
      {{a:hp}}       - прозрачность в зависимости от текущего здоровья (только в маркерах)
      {{a:hp-ratio}} - прозрачность в зависимости от процента текущего здоровья (только в маркерах)

  Примеры использования динамического цвета и прозрачности:
    "color": "{{c:hp-ratio}}" - цвет в зависимости от процента здоровья
    "alpha": "{{a:hp}}" - прозрачность в зависимости от количества здоровья
