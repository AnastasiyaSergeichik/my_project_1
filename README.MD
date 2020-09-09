# Отчет о тестировании приложения KeyValidator, проверяющее лицензионные ключи на валидность.
**Проведено:**
 - тестирование установки OpenJDK11 на Windows 10, его запуск и совместимость с Java 11, работает ли приложение согласно руководству пользования.
 - функциональное тестирование приложения KeyValidator на основе предоставленных для тестирования лицензионных ключей, а также совместимость приложения KeyValidator c Java 11

**Дата начала** - 08.09.2020

**Дата окончания** - 08.09.2020

**На тестирование затрачено** - 1,5 часа 

**В процессе тестирования использовались следующие артефакты:**
1. Инструкция по установке OpenJDK11 работает под ОС тестировщика
2. Приложение запускается и совместимо с Java 11
3. Приложение работает согласно руководству использования

**В результате тестирования выявлены следующие дефекты:**
1. Ключи из списка валидных оказались невалидными
 * 80b427f8-92cd-3aae-ba04-3927fbe17c6
 * 387eedc6-12e9-3b32-9881-63b6b5e85317

Ссылка [https://github.com/AnastasiyaSergeichik/my_project_1/issues/1](https://github.com/AnastasiyaSergeichik/my_project_1/issues/1)

2. Ключи из списка невалидных оказались валидными
 * 2fb98b44-93e7-3bdd-a2ad-79347bfe4ad1

Ссылка [https://github.com/AnastasiyaSergeichik/my_project_1/issues/2](https://github.com/AnastasiyaSergeichik/my_project_1/issues/2)

## Описание процесса тестирования
1. Скачать OpenJDK11 в соответствии с инструкцией по установке OpenJDK11 по [ссылке](https://github.com/netology-code/javaqa-homeworks/blob/master/intro/openjdk11-manual.md)
2. Протестировать установку OpenJDK11 через терминал выполнив команду java -version
3. Скачать приложение [KeyValidator.class](https://github.com/netology-code/javaqa-homeworks/blob/master/intro/user-manual.md)
4. Создать локальный репозиторий
5. Добавить в него файл [.gitignore](https://github.com/netology-code/javaqa-homeworks/blob/master/.gitignore) и файл с приложением KeyValidator
6. Запустить в терминале приложение KeyValidator командой java KeyValidator <ключ>, где <ключ> - передаваемые для валидации ключи

**В качестве тестовых данных использовались данные [https://github.com/netology-code/javaqa-homeworks/blob/master/intro/user-manual.md](https://github.com/netology-code/javaqa-homeworks/blob/master/intro/user-manual.md)**

## Ожидаемый результат:
* Result for <ключ>: OK - для валидных ключей
* Result for <ключ>: FAIL - для невалидных ключей

## Фактический результат:
**Валидные ключи:**

* 8f05e6a7-70e9-33d7-bfe7-b19eae0d8998 - OK
* 80b427f8-92cd-3aae-ba04-3927fbe17c6 - FAIL
* b295bc63-9f03-3b4b-af80-969b39f8c262 - OK
* 387eedc6-12e9-3b32-9881-63b6b5e85317 - FAIL
* c19a8cf9-5c3a-37c5-b7f3-d16d38a0c180 - OK

**Невалидные ключи:**
* 18252235-78e0-44a5-8720-556f0c7da17a - FAIL
* e66075b6-ddad-445e-baf6-161b3289522b - FAIL
* b6d53250-f07e-4352-a293-6102ddf7f1ca - FAIL
* c2bc778a-1cb9-46c6-b435-0489649d2a42 - FAIL
* 2fb98b44-93e7-3bdd-a2ad-79347bfe4ad1 - OK


**Тестирование производилось в следующем окружении:**
 notebook LG-book; 
 Windows 10;
 Java, Version 11.0.8; 
 Chrome, Version 84.0.4147.105
