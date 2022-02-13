# 📚Born2beRoot

Подробнее о проекте [en.subject.pdf](/en.subject.pdf)

Команды, которые мне пригодились при выполнении проекта [b2br.txt](/b2br.txt)

Цель проекта - настроить свой первый сервер, следуя определенным правилам.

Вы должны выбрать в качестве операционной системы либо последнюю стабильную версию Debian (без
тестирования/нестабильную), либо последнюю стабильную версию CentOS. Debian настоятельно рекомендуется, если вы новичок в системном администрировании.

Вы должны создать не менее 2 зашифрованных разделов с помощью LVM.
Во время защиты вам будет задано несколько вопросов о
выбранной вами операционной системе. Вы должны знать
разницу между aptitude и apt, или что такое SELinux или AppArmor.

Служба SSH будет работать только на порту 4242. По соображениям безопасности не должно быть
возможности подключиться с помощью SSH в качестве root.

Вы должны настроить свою операционную систему с помощью брандмауэра UFW и, таким образом, оставить открытым только
порт 4242. 

Имя хоста вашей виртуальной машины должно быть вашим именем входа, заканчивающимся на 42 (например,
ephantom42).

Во время защиты вам придется создать нового пользователя и назначить его
в группу.

Чтобы настроить надежную политику паролей, вы должны соответствовать следующим требованиям:
* Срок действия вашего пароля истекает каждые 30 дней.
* Минимальное количество дней, разрешенных до изменения пароля
, будет установлено равным 2.
* Пользователь должен получить предупреждающее сообщение за 7 дней до истечения срока действия его пароля.
* Ваш пароль должен содержать не менее 10 символов. Он должен содержать заглавную
букву и цифру. Кроме того, он не должен содержать более 3 последовательных одинаковых
символов. 
* Пароль не должен содержать имя пользователя.
* Следующее правило не применяется к паролю root: пароль должен содержать
не менее 7 символов, которые не являются частью предыдущего пароля.
* Конечно, ваш пароль root должен соответствовать этой политике.

Чтобы настроить надежную конфигурацию для вашей группы sudo, вы должны соответствовать
следующим требованиям:
* Аутентификация с использованием sudo должна быть ограничена 3 попытками в случае неправильного пароля.
* Пользовательское сообщение по вашему выбору должно отображаться, если
при использовании sudo возникает ошибка из-за неправильного пароля.
* Каждое действие с использованием sudo должно быть заархивировано, как входы, так и выходы. Файл журнала
должен быть сохранен в папке /var/log/sudo/.
* Режим TTY должен быть включен по соображениям безопасности.

Вам нужно создать простой скрипт под названием monitoring.sh . Он должен быть разработан в bash.
При запуске сервера скрипт будет отображать некоторую информацию (перечисленную ниже) на всех терминалах каждые 10 минут.
Ваш скрипт всегда должен иметь возможность отображать следующую информацию:
* Архитектура вашей операционной системы и версия ее ядра.
* Количество физических процессоров.
* Количество виртуальных процессоров.
* Текущая доступная оперативная память на вашем сервере и коэффициент ее использования в процентах.
* Текущая доступная память на вашем сервере и коэффициент ее использования в процентах.
* Текущий коэффициент использования ваших процессоров в процентах.
* Дата и время последней перезагрузки.
* Количество активных подключений.
* Количество пользователей, использующих сервер.
* IP-адрес вашего сервера и его MAC-адрес.
* Количество команд, выполненных с помощью программы sudo.