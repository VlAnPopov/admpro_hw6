# ДЗ 6 - Размещаем RPM в своём репозитории
Задачи:
* создать свой RPM (можно взять свое приложение, либо собрать к примеру апач с определенными опциями);
* создать свой репо и разместить там свой RPM;
* реализовать это все либо в вагранте, либо развернуть у себя через nginx и дать ссылку на репо.

Перечисленные задачи решаются скриптом assembly.sh, который запусается вагрантом. Для проверки работы репозитория из него устанавливается percona-orchestrator.