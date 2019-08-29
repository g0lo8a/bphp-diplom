# Дипломный проект по курсу Основы PHP

## «Разработка информационной системы Бюро переводов» 

Вы работаете над системой, которая автоматизирует работу бюро переводов. С системой взаимодействуют: менеджер, который принимает заказ на перевод, и переводчик.

### Бизнес-процесс (as is)

Сейчас в компании действуют следующие процессы:

1. Менеджер получает задание на перевод от заказчика;
1. Менеджер формирует задание в файл, который затем передает переводчику;
1. Переводчик получает задание и выполняет работу, затем отправляет файл менеджеру;
1. Менеджер проверяет работу:
    1. Есть необходимость доработки перевода — пересылает обратно переводчику;
    1. Если есть необходимость в переводе на дополнительный язык — отправляет переводчику с владением необходимого языка;
    1. Если все переводы есть и нет необходимости в доработках — передает заказчику результаты работы.


### Проблема
Чем больше становится клиентская база, тем больше мы привлекаем в работу переводчиков, тем менее эффективно используется время менеджера — серьезная часть времени уходит на пересылку файлов, а не на общение с клиентами, процесс становится мало предсказуемым и менее контролируемым - децентрализованное хранение данных, неочевидность текущей нагрузки переводчиков, как следствие хаотичное движение бумаг, отлынивание от обязанностей, споры по поводу обязательств и другие неблагоприятные для фирмы последствия.

### Решение
Разработка информационной системы «Бюро переводов».

### Необходимые возможности ИС
* Простое ведение задач:
    * Назначение исполнителя;
    * Назначение cрока выполнения;
    * Хранение неизменного текста оригинала;
    * Необходимые языки перевода;
    * Указание клиента;
    * Возможность отредактировать или удалить.
* Контролируемые списки заданий:
    * Список заданий, отсортированных по контрольному сроку;
    * Пометки статусов задач;
    * Фильтры задач по статусам;
    * Задачи, назначенные в работу одним переводчикам, недоступны другим переводчикам.

### Бизнес-процесс (to do)

С использованием системы процессы в компании будут работать так:

1. Менеджер получает задание на перевод от заказчика;
1. Менеджер создает задание в ИС «Бюро переводов»;
1. Переводчик видит задание и приступает к выполнению;
1. Переводчик вносит переводы в форму и отправляет на проверку;
1. Менеджер проверяет работу:
    1. Если есть необходимость доработки перевода — Делает возврат задачи переводчику;
    2. Если есть необходимость в переводе на дополнительный язык — изменяет исполнителя и сохраняет изменения в задаче;
    3. Если все переводы есть и нет необходимости в доработках — передает заказчику результаты работы.

### Прототип
Новый бизнес-процесс представлен на интерактивном прототипе, размещенном по ссылке https://yjtq42.axshare.com/.

*Сам прототип кликабелен, но функции сохранения/редактирования/удаления не работают.*

### Примеры выполненой работы:

Пример1. http://bphp.sdew.ru/

Интерфейс менеджера: 
Логин: test@test.ru
Пароль: 12345

Интерфейс переводчика:
Логин: mail@mail.ru
Пароль: qwerty

### Алгоритм разработки

1. Продумать архитектуру хранения данных;
1. Продумать структуру конфигурационных файлов;
1. Вынести в константы роли пользователей;
1. Разработать модуль авторизации;
1. Разработать модуль создания/редактирования заданий;
1. Разработать модуль просмотра списка заданий с разграниченным доступом по ролям;
1. Добавить в модуль создания задания функции редактирования задания;
1. Сделать возможным удаление заданий;
1. Разработать модуль выполнения задания;
1. Разработать модуль проверки выполненных заданий;
1. Отображать счетчики текущих заданий по переводчикам менеджеру при создании задания, для определения текущей нагрузки.

### Навыки необходимые для разработки
* Знание HTML;
* Знание языковых конструкций языка PHP.

### Критерии зачета (как понять, что диплом готов)
* Студент размещает файлы на сервер в свою папку. И предоставляет ссылку “Дипломный проект” и сообщает дпиломному руководителю.
* Дипломный руководитель проверяет работу 
* Задание считается выполненным, если:
    * В процессе работы ИС не возникает ошибок 4хх-5хх;
    * Выполнены все пункты задания из части "Алгоритм разработки";
    * Внешний вид ИС имеет некое стилевое оформление;
    * Логика работы ИС идентична логике работы прототипа.
    
### Как правильно задавать вопросы дипломному руководителю?
Что следует делать, чтобы все получилось:

1. Попробовать найти ответ сначала самому в интернете. Ведь, именно это скилл поиска ответов пригодится тебе на первой работе. И только после этого спрашивать дипломного руководителя.
2. В одном вопросе должна быть заложена одна проблема.
3. По возможности, прикреплять к вопросу скриншоты и стрелочкой показывать где не получается. Программу для этого можно скачать здесь https://app.prntscr.com/ru/.
4. По возможности, задавать вопросы в комментариях к коду. Начинать работу над дипломом как можно раньше! Чтобы было больше времени на правки.
5. Делать диплом по частям, а не все сразу. Иначе, есть шанс, что нужно будет все переделывать :).

Что следует делать, чтобы ничего не получилось:

1. Писать вопросы вида “Ничего не работает. Не запускается. Всё сломалось.”
2. Откладывать диплом на потом.
3. Ждать ответ на свой вопрос моментально. Дипломные руководители - работающие разработчики, которые занимаются, кроме преподавания, своими проектами. Их время ограничено, поэтому постарайтесь задавать правильные вопросы, чтобы получать быстрые ответы!
