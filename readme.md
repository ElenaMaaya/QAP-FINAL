Функциональное тестирование интернет-магазина Лабиринт.
Страница сайта интернет-магазина: https://www.labirint.ru/


Этот репозиторий содержит автотесты сайта интернет-магазина Лабиринт.
Тесты выполнены на Python 3.10 с применением PageObject и фреймворков Pytest и Selenium.
Тесты запускаются в браузере Chrome.


Файлы.
В папке .tests находятся автотесты для тестируемых страниц магазина.
В папке .pages находятся файлы с классами и методами для работы с соответствующими страницами сайта. 
Так же там находятся файлы с тестовыми данными, описаниями url сайта и вспомогательными методами.
В папку .tests/screenshots сохраняются скриншоты, создающиеся при выполнении тестов.

В browser_versions.txt описана версия браузера

Как запускать тесты.

Установить зависимости:

pip3 install -r requirements
Скачать Selenium WebDriver с https://chromedriver.chromium.org/downloads 
(выбрать версию, совместимую с вашим браузером) и скопировать в папку .chromedriver.

Запустить тесты можно:

из среды разработки PyCharm все тесты, создав тестовую конфигурацию pytest и указав папку .tests
из среды разработки PyCharm как отдельными тестами, так и одним файлом теста
из командной строки как файл теста, так и отдельный тест в файле:
pytest -v <test_file_name>::<test_name>


Команды для запуска тестов:

python -m pytest -v --driver Chrome --driver-path C://chromedriver/chromedriver.exe /tests/test_auth_page.py

python -m pytest -v --driver Chrome --driver-path C://chromedriver/chromedriver.exe /tests/test_header_btn.py

python -m pytest -v --driver Chrome --driver-path C://chromedriver/chromedriver.exe /tests/test_header_search.py

python -m pytest -v --driver Chrome --driver-path C://chromedriver/chromedriver.exe /tests/test_start_page.py


где C://chromedriver/chromedriver.exe находится путь к драйверу Selenium для текущей ОС

