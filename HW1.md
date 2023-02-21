CAP теорема и некотрые СУБД
1) DragonFly
DragonFly относится к AC (availability, consistency), этому свидетельствует их официальный сайт с документацией, согласно CAP теореме, на официальном сайте данной СУБД как раз и прослеживается описание согласованности и доступности:

For example the HAMMER filesystem, the default in DragonFly BSD, is the most powerful and reliable filesystem available on any operating system. It can handle up to an exbibyte of files (or, 1048576 tebibytes) and can automatically recover without the need for a fsck.
…
Because the source code for DragonFly itself is generally available, the system can also be customized to an almost unheard-of degree for special applications or projects, and in ways not generally possible with operating systems from most major commercial vendors.

2) ScyllaDB
Данную СУБД можно отнести к AP (availability, partition tolerance) хотя бы потому, что ScyllaDB заимствует многие характеристики Cassandra, которая в свою очередь является AP системой. Но если рассмотреть ScyllaDB отдельно, рассмотрев документацию на официальном сайте, то можно понять, что как раз в ущерб согласованности данная СУБД устойчива к разделению и доступна, т.е. система будет продолжать функционировать в случае задержки или отбрасывания сообщения узлами.

ScyllaDB Cloud is available on both AWS and Google Cloud public clouds, so you can choose your preferred cloud provider to run your cluster.

Также статья из официального блога может подтвердить слова выше.

3) ArenadataDB
ArenadataDB можно отнести к CP (consistency and partition tolerance), это подверждает данный сайт и видео-обзор СУБД.

Какие наиболее значимые функциональные особенности есть у Arenadata DB?

Транзакционность (ACID).
Возможность организации хранения данных таблиц как по строкам, так и по столбцам.
Механизм резервного копирования и восстановления с параллельным выполнением на всех узлах кластера.
Возможность партиционирования таблиц с указанием различной ориентации (колоночная/строковая) и различных типов и параметров компрессии для каждой из партиций.
Возможность параллельной записи данных в сегменты кластера.
Возможность управления ресурсными квотами и очередями, наличие механизма ресурсных групп для квотирования ресурса CPU и RAM.
Поддержка стандарта ANSI SQL версии 2008 или выше.
Наличие эффективных алгоритмов сжатия данных (например, Z_Standart), возможность выбора типа и уровня компрессии.
Наличие встроенного инструмента моделирования и анализа данных, позволяющего строить линейную регрессию и нейронную сеть.
Поддержка различных аппаратных архитектур x86/64 и IBM Power.
