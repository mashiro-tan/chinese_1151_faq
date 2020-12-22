### Термины и жаргонизмы: 
*Кофемод* – модификация материнской платы (на базе чипсета 100 и 200 серии) и прошивки BIOS для обеспечения совместимости с процессорами i3…i9 8ххх-9ххх. Чаще всего прошивать BIOS приходится с помощью программатора. 

*Кофейник* – процессор 8 или 9 поколения Intel (СoffeLake). 

*Пин-мод* – изоляция одних и закорачивание других контактов на процессоре, согласно известной схеме.  Однако, иногда изоляции может потребоваться меньше или не потребоваться вовсе. Чтобы это определить, проверьте отсутствие КЗ на землю для каждого отмеченного для вашей платы контакта в сокете. Пины, «звонящиеся» на землю, изолировать нужно. Для удобства вместо перемычки на процессоре можно сделать перемычку на материнской плате, нужные контакты так же выявляются диодной прозвонкой. Есть вариант физического удаления ножек из сокета, что не повлияет на дальнейшую работоспособность. 

*CT, КТ, CoffeeTime, кофетайм* – программа для модифицирования прошивки BIOS, с целью добавления нужных микрокодов, патчей, персональной информации и прочих полезностей с целью получения совместимости с 8 и 9 поколением процессоров Intel. На данный момент актуальны две версии: 0,9 – с графическим интерфейсом, но это полностью ручной режим эксперта, без подсказок, имеет два вида патча для совместимости со склейками. 0,85а – классическая версия, в командной строке, автоматическая модификация, есть режим эксперта, перенос персональных данных работает в обоих версиях. Спасибо svarmod за это. 

*Пердосклейка (склейка)* – ноутбучный процессор, напаянный на переходник для установки в десктопный сокет. Может быть как инженерным образцом, так и серийным. 

*Инженерник (ES)* - опытный образец процессора. Они являются предпроизводственными процессорами, которые корпорация Intel предоставляет производителям комплектного оборудования (OEM), производителям оригинальных устройств и прочим для использования в цикле проектирования продукции перед запуском продукта. Часто имеют заниженные частоты, худший разгонный потенциал ядер и памяти, иметь нерабочее встроенное видеоядро, битый контроллер PCIe (не работает дискретная видеокарта) и прочие неприятные сюрпризы. Чем более ранняя версия инженерника, тем больше проблем может быть с ним. 

*Порт-биос* – адаптированная версия BIOS от совместимой Z370 материнки для Z270, если такая существует. Удачный исход позволит запускать на ней все CoffeeLake процессоры. Метод применим и для не-Z материнок. Позволяет запускать 8 ядерные процессоры с НТ. Известно о существующих набора порт-биосов для материнских плат ASUS. Существуют и для других вендоров (курение форумов обязательно).  

*Пердолинг* – героический процесс решения проблем с обеспечением работоспособности и/или повышением производительности компьютерного железа (как правило, проблемы создаются самим юзверем). 


### А теперь ближе к теме. 
В материнские платы 1151 можно установить процессоры CoffeeLake 8ххх-9ххх (без проблем работают с DDR3 и DDR3L памятью). Для установки требуется модификация биоса и физически замкнуть/заизолировать контакты на самом процессоре. Основная проблема в биосах разных плат – это ограничение максимального количества поддерживаемых процессорных потоков. Но если, например, на плате можно запустить 9700К, то на ней также заработает и 9900К с выключенным HT. Решается выбором материнской платы, для которой имеется порт-биос от Z370. 

Для плат на базе чипсетов Z370, B365 и H310C можно добавить поддержку процессоров Skylake и KabyLake. Для этого достаточно понизить версию МЕ и добавить необходимые микрокоды. 

Установка пердосклеек требует прямых рук. Если у вас не руки, а лапки - вам в другие треды. У склеек голый кристалл, а значит, нужен охлад с цельной медной подошвой, и есть опасность сколоть кристалл при установке этого самого охлада. У десктопных инженерников обычная крышка - у них таких заморочек нет. 

Для CoffeeLake non-K ES есть ограничения по разгону памяти в зависимости от ревизии: U0 - до 2666 МГц, P0 - до 3333 МГц, для QQBZ и всяких QN8H актуально. 

Если собрались брать «кофейник» - обязательно читать тему на форуме overclockers.ru, внимательное изучение шапки темы обязательно https://forums.overclockers.ru/viewtopic.php?f=1&t=602278 
 
### Группировка по процессорам. 
Если вашего здесь нет - идем спрашивать в тред
 
#### Уровень сложности – 0 perd 
Не требуется модификация BIOS, не требуется особый кулер, не требуется пин-мод. Для понижения версии BIOS потребуется программатор. BIOS определенной, не последней версии.  

i7-6400T (QHQG, QHQJ, QHQF), (4C/8T). инженерные образцы i7-6700 (K). Легендарный инженерник в свое время, а ныне незаслуженно забытый, классика 2016 года, если удастся купить по небольшой цене – вполне себе годный вариант, особенно, если вместо рук – лапки. Материнка на Z-чипсете крайне предпочтительна, т.к. базовая частота может быть очень низкой. Разгон по шине ~4 ГГц. Только 100 серия чипсетов. Подробнее по ссылке: https://forums.overclockers.ru/viewtopic.php?f=2&t=563272 
Процессоры i3, i5 и i7 поколения Skylake и KabyLake. Серийные модели, вставил и забыл, если за недорого удастся купить – почему бы и нет? Основная проблема процессоров – дороговизна. 

#### Уровень сложности – Easy perd 
Требуется модификация BIOS в кофетайме. Пин-мод не требуется. Особый кулер не требуется. 

Список процессоров (2C/4T): гиперпни G49XX-G5XXX, (4C/4T): i3-8100, i3-8100T, i3-8300, i3-8300T, i3-8350K, i3-9100, i3-9100T, i3-9100F (SRF7W), i3-9300, i3-9300T, i3-9320, i3-9350KF.  

Наиболее интересная модель – i3-9100F со степпингом B0, на крышке маркировка SRF7W. Прошил BIOS, вставил и поехали. 
 
#### Уровень сложности – Normal perd 
Требуется модификация BIOS в кофетайме. Требуется пин-мод, Особый кулер не требуется. Для 16 поточных моделей чаще всего требуется порт-BIOS, совместимы не со всеми материнками. 

Серийные и инженерные экземпляры 8ххх, 9ххх (K, F, KF) (6/6, 6/12, 8/8, 8/16), возможен разгон К-моделей. 
 
(6/12) Наиболее интересные инженерные модели процессоров: QN8G (8700K), QN8H, QNLW, (8700 ES) QN8J (8700T ES). QNLV – покупать с осторожностью, есть отчеты анонов о плохом разгонном потенциале. 

Для К-моделей материнка обязателен Z-чипсет, ибо процы могут в разгон памяти, и этот разгон даст хороший прирост производительности. Есть куча готовых бивасов, рукастые могут сделать бивас сами кофетаймом. Совместимость не со всеми мамками (как и все кофейники). Разлоченные процы в разгоне сильно греются и требуют хороший охлад. 
 
(8/16) Наиболее интересные инженерные модели процессоров: QQBY (i9-9900K ES), QQBZ (i9-9900 ES), QQC0 (i9-9900T ES) – 8 ядерные 16 поточные процессоры и их инженерные версии, c этими процессорами есть нюансы, читайте тему на оверах опять же! 
 
#### Уровень сложности – Hard perd 
Склеечки. Требуется модификация BIOS в кофетайме 0,9 или готовый от китайца-продавца. Пин-мод **не требуется**. Требуется кулер с ровной медной/никелированной подошвой (**НЕ директконтакт**) и повышенные требования к радиусу кривизны рук. Крепеж кулера только на подпружиненных винтах или с жесткими упорами под лапы кулера. 

### Склейки
#### KabyLake
QL2X (курлыкс) (4C/8T) – склейка, является инженерной версией Core i7-7820hk, 4 ядра, 8 потоков, архитектура KabyLake, стоковые частоты 2,7 ГГц, буст: 3,8 ГГц, разгон до 4,3-4,5+ ГГц, встройка HD Graphics 630. Разгон памяти, как правило, ограничен 3000 МГц.  

QL3X (курлыкс) (4C/8T) – склейка, архитектура KabyLake, стоковые частоты: 2,4 ГГц, буст: 3,5 ГГц, разгон до 4,0-4,2+ ГГц, встройка HD Graphics 630. Разгон памяти, как правило, ограничен 3000 МГц. Имеет меньшие начальные частоты, меньший разгонный потенциал, но и стоит дешевле. 

Под данные камни хватит платы и на H110 чипсете (но для хорошего разгона нужен серьезный питальник). Есть куча готовых бивасов в группе «купи дешево», рукастые могут собрать BIOS сами по инструкции с YouTube. 

Проблемы - память не особо гонится, при серьезном разгоне требуется хороший охлад. 

QNCT (кунст, кунт) (6C/12T) – склейка является инженерной версией Core i7-8850H, архитектура CoffeeLake стоковые частоты: 2,4 ГГц, буст 2.8 ГГц, встройка HD Graphics 630. Разгон ядер лишь до 3,3 ГГц через утилиту XTU. Память чаще всего не гонится выше 2666 МГц.  

Хватит мамки и на H110, а из-за того, что проц залочен и имеет TDP всего в 45 Вт, то и с питальником материнки заморачиваться не стоит, как и с охладом - хватит простого кулера «а-ля боксовый». В утилите Intel Extreme Tuning Utility (XTU) можно повысить частоту всех ядер до 3,3, выставить увеличенные лимиты потребления. Но нужно делать профиль в программе и автозапуск с другим приложением (MSI Afterburner например).  

Проблемы - совместим не со всеми мамками (как и все кофейники). Готовые бивасы есть, но мало (а бивасы от продавца-китайца не всегда рабочие), но можно на форуме оверклокерсов в теме кофетайма попросить помощи. Память не особо гонится. 

#### CoffeeLake
QQLT (кукульт) (6C/12T) – склейка является инженерной версией i9-9850HK, стоковые частоты: 2,4 ГГц, буст: 4,1 ГГц, разблокированный множитель, Разгон ~4,9 ГГц. Материнку обязательно на Z-чипсете. 

Проблемы - совместим не со всеми мамками (как и все кофейники). Бивасов пока ПАРА штук, поэтому или пинаем продавца-китайца (не факт, что китаец пришлет рабочий BIOS) или опять-таки идем за помощью на форум оверов. При разгоне процы жрут и греются также как и десктопные образцы – нужен хороший кулер.  

Интересная (уже нет) материнская плата на момент написания гайда - ASUS Z170I PRO GAMING, ибо продается (уже нет) новая в магазинах примерно за 5,5к (уже нет), и на нее есть биосы под все процы в гайде. Проблема с этой мамкой только одна - для прошивки нужен программатор, но благо микруха биваса извлекаемая. Так же заслуживают внимания платы серии Maximus VIII и IX, с ними меньше всего проблем по совместимости с инжами и склейками. Можно обратить внимание на гигабайты - шьются стандартными средствами. 

В CoffeeTime 0.9 в разделе Extra есть два вида патча для склеек, определить работающий вариант можно опытным путем. Нужны тесты добровольцев! 

QQLS (кукульсик) (8C/16T) – склейка является инженерной версией i9-9980HK, архитектура CoffeeLake стоковые частоты: 2,1 ГГц, буст 4.4 ГГц. Разгон ~4.9 ГГц, потребление 200 Вт. Разгон памяти обычно ограничивается частотой 3000 МГц. 

В CoffeeTime 0,9 можно попробовать собрать себе BIOS самостоятельно на основе версии 2ххх. Для QQLS не нужен фикс дискретки, информация от svarmod. Чтобы 16-поточник заработал, использовать для модификации ME COR 11.7.0.3307, HAP-bit, микрокод 906EC, и остальные патчи, которые требуются для запуска обычных серийных CoffeeLake, возможно есть шанс запустить 16 потоков на версии биоса 3805, но с ограничениями. QQLS, как и все 8/16 обладает ограниченной совместимостью с материнскими платами. 

Инструкция по запуску QQLS на материнке ASUS Z170i Pro Gaming: https://forums.overclockers.ru/viewtopic.php?p=17037813#p17037813 

#### CometLake
\*по заявлением китайцев, по ревизии проходит как коферефреш (?)
QTJ2 (6/12T) - блокированный множитель, является чем-то средним между QQLT и QNCT благодаря заметно более высоким стоковым частотам. Обзор https://mysku.ru/blog/aliexpress/83730.html

QTJ1 (8/16T) - почти то же, что и QQLS, дороже на тыщу-полторы. Детали неизвестны. По ссылке выше также заявлен QTJ0, также с разблокированным множителем и повыше стоковыми частотами.

### LGA1200

QVJ1 (8/16T) - Рокетлейк, аналог 11900, пока вроде только на таобао, сравнение на китайском здеся https://www.163.com/dy/article/FUDE1ALI0512MJDN.html

#### Ссылкота

Профильная тема на overclockers.ru, **ИДИ ЧИТАЙ ШАПКУ**: https://forums.overclockers.ru/viewtopic.php?f=1&t=602278

Профильная тема паблика "продай мамашу", источник инфы из первых рук (и ног): https://vk.com/topic-114738215_41374166

Список инженерников для 1151 и 1151v2 сокета. https://anonfile.com/B4t6f3s3b8/1151ES_pdf   
  
Хорошие поставщики недорогих процессоров на Ali: 
 1. Пердосклейщик https://aliexpress.ru/store/5940103 
 2. Ming&Yang Store https://aliexpress.ru/store/1084128 
 3. А больше и нет никого, хайп на удивление пока только начался.
  
Полезные ссылки: 

Программатор с прищепкой: https://aliexpress.ru/item/32898599200.html 

Биосы под склейки: https://cloud.mail.ru/public/3Sea/5CFfmrn5m/ 

Скачать Intel Extreme Tuning Utility (XTU): https://downloadcenter.intel.com/download/29183/Intel-Extreme-Tuning-Utility-Intel-XTU 

Скачать CoffeeTime 0.85a: https://yadi.sk/d/i4FE9b-o3apk5b 

Обязательно для корректной работы процессоров, особенно это касается степпинга R0, требуется разархивировать содержимое CoffeTime.085-add_MC by Michael_Code в папку с CoffeeTime 0.85a с заменой файлов. Данный архив содержит актуальные рабочие микрокоды D2: https://yadi.sk/d/GIJfqzJeoKP6yQ 

Скачать CoffeeTime 0.9: https://yadi.sk/d/yx56sT4me49yHA 

Тема на форуме от создателя порт-биосов dsanke (без приглашения регистрация платная, а без регистрации скачивать нельзя): http://www.smxdiy.com/thread-2389-1-9.html 
