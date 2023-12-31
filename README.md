# Общие команды
- `\copyright` - отображение условий использования и распространения PostgreSQL.
- `\crosstabview [COLUMNS]` - выполнение запроса и отображение результатов в форме кросс-таблицы.
- `\errverbose` - отображение самого последнего сообщения об ошибке с максимальной подробностью.
- `\g [(OPTIONS)] [FILE]` - выполнение запроса (и отправка результатов в файл или |pipe); `\g` без аргументов эквивалентно точке с запятой.
- `\gdesc` - описание результата запроса без его выполнения.
- `\gexec` - выполнение запроса, а затем выполнение каждого значения в его результате.
- `\gset [PREFIX]` - выполнение запроса и сохранение результатов в переменных psql.
- `\gx [(OPTIONS)] [FILE]` - как `\g`, но с принудительным расширенным режимом вывода.
- `\q` - выход из psql.
- `\watch [SEC]` - выполнение запроса каждые SEC секунд.

# Справка
- `\? [commands]` - отображение справки по командам в обратной косой черте.
- `\? options` - отображение справки по параметрам командной строки psql.
- `\? variables` - отображение справки по специальным переменным.
- `\h [NAME]` - справка по синтаксису SQL-команд, * для всех команд.

# Буфер запроса
- `\e [FILE] [LINE]` - редактирование буфера запроса (или файла) во внешнем редакторе.
- `\ef [FUNCNAME [LINE]]` - редактирование определения функции во внешнем редакторе.
- `\ev [VIEWNAME [LINE]]` - редактирование определения представления во внешнем редакторе.
- `\p` - отображение содержимого буфера запроса.
- `\r` - сброс (очистка) буфера запроса.
- `\s [FILE]` - отображение истории или сохранение ее в файл.
- `\w FILE` - запись буфера запроса в файл.

# Ввод/вывод
- `\copy ...` - выполнение SQL COPY с потоком данных на клиентском хосте.
- `\echo [-n] [STRING]` - запись строки в стандартный вывод (-n для отсутствия новой строки).
- `\i FILE` - выполнение команд из файла.
- `\ir FILE` - как \i, но относительно расположения текущего сценария.
- `\o [FILE]` - отправка всех результатов запроса в файл или |pipe.
- `\qecho [-n] [STRING]` - запись строки в поток вывода \o (-n для отсутствия новой строки).
- `\warn [-n] [STRING]` - запись строки в стандартный поток ошибок (-n для отсутствия новой строки).

# Условные операторы
- `\if EXPR` - начало условного блока.
- `\elif EXPR` - альтернатива в пределах текущего условного блока.
- `\else` - окончательная альтернатива в пределах текущего условного блока.
- `\endif` - завершение условного блока.

# Информация
- `\d[S+]` - список таблиц, представлений и последовательностей.
- `\d[S+] NAME` - описание таблицы, представления, последовательности или индекса.
- `\da[S] [PATTERN]` - список агрегатов.
- `\dA[+] [PATTERN]` - список методов доступа.
- `\dAc[+] [AMPTRN [TYPEPTRN]]` - список классов операторов.
- `\dAf[+] [AMPTRN [TYPEPTRN]]` - список семейств операторов.
- `\dAo[+] [AMPTRN [OPFPTRN]]` - список операторов семейств.
- `\dAp[+] [AMPTRN [OPFPTRN]]` - список функций поддержки семейств операторов.
- `\db[+] [PATTERN]` - список таблиц-пространств.
- `\dc[S+] [PATTERN]` - список преобразований.
- `\dC[+] [PATTERN]` - список приведений.
- `\dd[S] [PATTERN]` - отображение описаний объектов, не отображаемых в других местах.
- `\dD[S+] [PATTERN]` - список доменов.
- `\ddp [PATTERN]` - список привилегий по умолчанию.
- `\dE[S+] [PATTERN]` - список внешних таблиц.
- `\des[+] [PATTERN]` - список внешних серверов.
- `\det[+] [PATTERN]` - список внешних таблиц.
- `\deu[+] [PATTERN]` - список отображений пользователей.
- `\dew[+] [PATTERN]` - список внешних оболочек данных.
- `\df[anptw][S+] [FUNCPTRN [TYPEPTRN ...]]` - список [только агрегатов/обычных/процедур/триггеров/оконных] функций.
- `\dF[+] [PATTERN]` - список конфигураций текстового поиска.
- `\dFd[+] [PATTERN]` - список словарей текстового поиска.
- `\dFp[+] [PATTERN]` - список парсеров текстового поиска.
- `\dFt[+] [PATTERN]` - список шаблонов текстового поиска.
- `\dg[S+] [PATTERN]` - список ролей.
- \di[S+] [PATTERN] - список индексов.
- `\dl` - список больших объектов, аналогично \lo_list.
- `\dL[S+] [PATTERN]` - список языков программирования.
- `\dm[S+] [PATTERN]` - список материализованных представлений.
- `\dn[S+] [PATTERN]` - список схем.
- `\do[S+] [OPPTRN [TYPEPTRN [TYPEPTRN]]]` - список операторов.
- `\dO[S+] [PATTERN]` - список упорядочиваний.
- `\dp [PATTERN]` - список привилегий на доступ к таблицам, представлениям и последовательностям.
- `\dP[itn+] [PATTERN]` - список [только индексов/таблиц] разделенных отношений [n=вложенных].
- `\drds [ROLEPTRN [DBPTRN]]` - список настроек роли на базу данных.
- `\dRp[+] [PATTERN]` - список публикаций репликации.
- `\dRs[+] [PATTERN]` - список подписок репликации.
- `\ds[S+] [PATTERN]` - список последовательностей.
- `\dt[S+] [PATTERN]` - список таблиц.
- `\dT[S+] [PATTERN]` - список типов данных.
- `\du[S+] [PATTERN]` - список ролей.
- `\dv[S+] [PATTERN]` - список представлений.
- `\dx[+] [PATTERN]` - список расширений.
- `\dX [PATTERN]` - список расширенных статистик.
- `\dy[+] [PATTERN]` - список триггеров событий.
- `\l[+] [PATTERN]` - список баз данных.
- `\sf[+] FUNCNAME` - отображение определения функции.
- `\sv[+] VIEWNAME` - отображение определения представления.
- `\z [PATTERN]` - то же, что и \dp.

# Форматирование
- `\a` - переключение между выравниванием и не выравниванием режима вывода.
- `\C [STRING]` - установка заголовка таблицы или отмена, если отсутствует.
- `\f [STRING]` - отображение или установка разделителя полей для не выравниваемого вывода запроса.
- `\H` - переключение режима HTML-вывода (в настоящее время выключено).
- `\pset [NAME [VALUE]]` - установка параметра вывода таблицы.
- `\t [on|off]` - отображение только строк (в настоящее время отключено).
- `\T [STRING]` - установка атрибутов тега HTML <table> или отмена, если отсутствует.
- `\x [on|off|auto]` - переключение расширенного режима вывода (в настоящее время выключено).

# Соединение
- `\c[onnect] {[DBNAME|- USER|- HOST|- PORT|-] | conninfo}` - подключение к новой базе данных (в настоящее время "test").
- `\conninfo` - отображение информации о текущем подключении.
- `\encoding [ENCODING]` - отображение или установка клиентской кодировки.
- `\password [USERNAME]` - безопасное изменение пароля для пользователя.

# Операционная система
- `\cd [DIR]` - изменение текущего рабочего каталога.
- `\setenv NAME [VALUE]` - установка или снятие установки переменной среды.
- `\timing [on|off]` - переключение отображения времени выполнения команд (в настоящее время выключено).
- `\! [COMMAND]` - выполнение команды в оболочке или запуск интерактивной оболочки.

# Переменные
- `\prompt [TEXT] NAME` - запрос у пользователя установки внутренней переменной.
- `\set [NAME [VALUE]]` - установка внутренней переменной или отображение всех, если нет параметров.
- `\unset NAME` - снятие установки внутренней переменной.

# Большие объекты
- `\lo_export LOBOID FILE` - экспорт большого объекта в файл.
- `\lo_import FILE [COMMENT]` - импорт файла в большой объект.
- `\lo_list` - список операций с большими объектами.
- `\lo_unlink LOBOID` - операции с большими объектами.

