# ❗ Информация для проверяющих

Здравствуйте!<br/>

Уязвимость в приложении заключалась в том, что при ```http``` запросе картинки передавался ```referer```, заголовок который в get параметрах передавал параметры запуска пользователей.<br/>

Для решения конкретно данного кейса можно использовать аттрибуты ```rel="noreferrer"``` ```referrerPolicy="no-referrer"``` конкретно для ```<img>``` тега. <br/>

Для более глобального решения проблемы, можно использовать специальный ```meta``` тег для всего html документа.  Например:  ```<meta name="referrer" content="same-origin">```.
