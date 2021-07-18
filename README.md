# Тестовое задание

Представим себе, что мы продуктовая компания, пишем ПО для каких-то предприятий.
В результате анализа потребностей клиентов компания пришла к выводу, что у предприятий существует потребность в качественном
обучении сотрудников. У компании уже есть некоторое количество походящих учебных курсов и научно-исследовательский потенциал для создания новых.

ЗАДАЧА:
Нужно написать сервис, предоставляющий API для доступа сотрудников к учебным курсам. 
Писать подробный код не нужно. Код пишем с точки зрения внутреннего устройства сервиса, определяя метода, но их реализацию в нижних слоях не пишем.
Например: В методе контроллера при запросе на получение сущности нужно закодировать получение сущности, например, через какой-то сетрвис. Но сам метод получения этой сущности в этом сервисе мы просто определяем, а в phpdoc пишем что это за метод, и что он делает. В контроллере нужно предусмотреть правильные коды ответа на случай, ели сущность существует, или ее нет. Таким образом и остальное.

 Требования к выполнению
 - Язык php >= 7.3 или Go 1.11.*
 - Желательно MVC
 - Писать подробный код не нужно. 
 - Должны использоваться интерфейсы 
 - доступ к курсам предоставляется в виде одноразовых ссылок. После прохождения курса ссылка недействительна. Одна ссылка - доступ к единственному курсу на одно прохождение.
 - Процесс прохождения курса - полностью фронтовая задача, мы пишем только бэкенд
      В процессе прохождения курса с фронта приходят запросы с инфой о процессе прохождения. Процесс прохождения курса - это когда курс пройден от 10 до 90 процентов. 
      В конце прохождения (100%) курс (фронт) отправляет на бек запрос, означающий, что курс пройден, значит ссылку делаем недействительной.
      (соответственно эту логику придется описать в коде, но как можно проще)
 - Учебный курс - сущность со свойствами id, name. Все остальные детали мы опустим.
 
 Методы, которые должны быть у сервиса:
 - Получене курса по одноразовой ссылке. Принимает имя сотрудника и название его предприятия.
 - Фиксация состояния процесса прохождения курса сотрудником.
 - Фиксация окончания прохождения курса. Этот метод можно совместить с прдыдущим, а можно сделать отдельным.
 
 
 Требовния к коду:
 - Соблюдать конецпцию тонких контроллеров.
 - Наличие сервисного слоя.
 - Чистый код, psr12
 
 Будет плюсом:
  - Запуск сервиса через docker-compose up
  
 Время на работу: 60-90 минут
