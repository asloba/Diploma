[План автоматизации](https://github.com/asloba/Diploma/blob/master/docs/Plan.md)

[Отчёт по итогам тестирования](https://github.com/asloba/Diploma/blob/master/docs/Report.md)

[Отчёт по итогам автоматизации](https://github.com/asloba/Diploma/blob/master/docs/Summary.md)
___

## Процедура запуска авто-тестов

### Перед запуском тестов необходимо установить окружение:

* OpenJDK 11.010
* Docker Desktop
* IntelliJ IDEA

### Запуск:

* Склонировать [код](https://github.com/asloba/Diploma) проекта
* Запустить Docker Desktop
* Открыть терминал в папке с проектом или в IntelliJ IDEA
* Выполнить  
  `docker-compose up `
* В новой вкладке терминала запустить приложение aqa-shop.jar командой  
  `java -jar ./artifacts/aqa-shop.jar`
* В новой вкладке терминала запустить автотесты командой  
  `./gradlew clean test`
* Cгенерировать отчёт Allure командой
  `./gradlew allureServe`

### По умолчанию проект запускается с БД MySQL

### Для запуска проекта на  PostgreSQL:

* Остановить приложение запущенное ранее в терминале командой ctrl + c
* В файле application.properties заменить `spring.datasource.url=jdbc:mysql://localhost:3306/app` на `spring.datasource.url=jdbc:postgresql://localhost:5432/app`
* В новой вкладке терминала запустить приложение aqa-shop.jar командой  
  `java -jar ./artifacts/aqa-shop.jar`
* В новой вкладке терминала запустить автотесты командой  
  `./gradlew clean test`
*  Cгенерировать отчёт Allure командой
    `./gradlew allureServe`
