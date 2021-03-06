# Отчет по итогам тестирования

**Описание:**

В процессе работы были протестированы следующие функции приложения:

1) Возможность купить тур по дебетовой карте;
2) Оформление тура в кредит;
3) Взаимодействие приложения с банковскими серверами;
4) Взаимодействие приложения с заявленными СУБД (MySQL и PostgreSQL).

**Количество тест-кейсов:** 44

**% успешных/неуспешных:** 54,54% / 45,46%

На скриншоте ниже представлен отчет Allure по итогам тестирования:

![mysqlallure](https://image.prntscr.com/image/6sHOlGwGSZK5JpJGX2-Vbg.png)

**Общие рекомендации:**

1. Необходимо доработать процесс взаимодействия приложения с СУБД, поскольку информация о совершенном платеже сохраняется лишь в отношении карт, данные которых были представлены разработчиками для теста.
2. Также стоит уделить отдельное внимание форме ввода данных, а именно полям:
  * "Владелец": На настоящий момент данное поле можно заполнить любыми значениями, что показывают тесты, и приложение будет принимать их в качестве валидных.
  * "Номер карты": На данный момент можно оплатить тур или отправить заявку на кредит только с картой, номер которой состоит из 16-ти символов. Однако у других платежных систем количество цифр в номере карты может отличаться. Например, номер карты Maestro состоит из 18-ти символов