# Введение

> Примечание: это издание книги так же, как и [The Rust Programming Language] доступно в печатном и электронном виде от [No Starch Press] .

Добро пожаловать в *The Rust Programming Language*, вводную книгу о Rust. Язык программирования Rust помогает создавать быстрые, более надёжные приложения. Хорошая эргономика и низкоуровневый контроль часто являются противоречивыми требованиями для дизайна языков программирования; Rust бросает вызов этому конфликту. Благодаря сбалансированности мощных технических возможностей и большого опыта разработчиков, Rust предоставляет возможности управления низкоуровневыми элементами (например, использование памяти) без трудностей, традиционно связанными с таким контролем.

## Кому подходит Rust

Rust подходит для многих людей по разным причинам. Приведём несколько самых важных групп.

### Команды разработчиков

Rust обеспечивает эффективные средства для совместной работы больших команд разработчиков с различным уровнем знаний системного программирования. Низкоуровневый код подвержен множеству незаметных ошибок, которые в большинстве других языков могут быть найдены только в результате обширного тестирования и тщательного анализа кода опытными разработчики. В Rust компилятор играет роль привратника, отказываясь компилировать код с этими неуловимыми ошибками, включая ошибки параллелизма. Компилятор позволяет команде разработчиков больше сосредоточить своё внимание на логике, а не терять время на поиски ошибок.

Rust также предлагает современные инструменты разработки для системного программирования:

- Cargo, встроенный менеджер зависимостей и инструмент сборки,  добавляет, компилирует и управляет зависимостями безболезненно и согласованно, используя экосистему Rust.
- Rustfmt обеспечивает согласованный стиль кодирования для всех разработчиков.
- Rust Language Server поддерживает интегрированную среду разработки (IDE) с автодополнением кода и встроенными сообщениями об ошибках.

Эти и другие инструменты экосистемы Rust, обеспечивают  разработчикам продуктивность при написании кода системного уровня.

### Студенты

Rust полезен для студентов и тех, кто заинтересован в изучении  системных концепций. Используя Rust, многие люди узнали о таких темах, как разработка операционных систем. Сообщество радушно и с удовольствием ответит на вопросы начинающих. Благодаря усилиям, таким как эта книга, команды Rust хотят сделать концепции систем более доступными для большего числа людей, особенно для новичков в программировании.

### Компании

Сотни компаний, больших и малых, используют Rust для различных целей. Эти задачи включают в себя инструменты командной строки, веб-сервисы, инструменты DevOps, встраиваемые устройства, анализ и транскодирование аудио и видео, крипто-валюты, био-информатика, поисковые системы, приложения интернета вещей, машинное обучение и даже основные части браузера Firefox.

### Разработчики Open Source

Rust для людей, которые хотят построить язык программирования Rust, сообщество, инструменты разработчика и библиотеки. Мы хотели бы, чтобы вы внесли свой вклад в развитие языка Rust.

### Люди, которые ценят скорость и стабильность

Rust для людей, которые жаждут скорости и стабильности в языке. Под скоростью здесь мы подразумеваем и скорость программ, которые вы можете создать с помощью Rust, и скорость с которой Rust позволяет вам написать их. Проверки компилятора Rust обеспечивают стабильность через добавление функций и рефакторинг. Это в корне отличается от хрупкого устаревшего кода на языках без таких проверок, который разработчики часто боятся изменить. Стремясь к абстракциям с нулевой стоимостью, компилируя высокоуровневые функции в код более низкого уровня так же быстро, как код, написанный вручную, Rust стремится сделать безопасный код также и быстрым.

Язык Rust надеется также на поддержку многих других пользователей (здесь упомянуты только несколько крупнейших заинтересованных сторон). В целом, величайшая важность Rust заключается в устранении компромиссов, которые программисты принимали десятилетиями, обеспечивая безопасность *и* производительность, скорость *и* эргономику. Попробуйте Rust и посмотрите, работает ли это для вас.

## Для кого эта книга

В этой книге предполагается, что вы уже писали код на другом языке программирования, но не делается никаких предположений о том, на каком. Мы пытались сделать материал хорошо доступным для тех, кто имеет большой опыт в программировании. Мы не тратим много времени на разговоры о том, *что такое* программирование или как думать об этом. Если вы новичок в программировании, вам больше подойдёт чтение книг, в которых содержится введение в программирование.

## Как использовать эту книгу

В целом, эта книга предполагает, что вы читаете её последовательно от начала до конца. Более поздние главы основываются на концепциях предыдущих. Иногда более ранние главы могут не углубляться в детали темы; мы обычно возвращаемся к теме в следующей главе.

В этой книге вы найдёте два вида глав: концептуальные главы и главы проекта. В концептуальных главах вы узнаете об аспектах Rust. В главах проекта мы будем вместе строить небольшие программы, применяя то, что вы узнали. Главы 2, 12 и 20 являются главами проекта; остальные являются концептуальными главами.

В главе 1 объясняется, как установить Rust, написать программу “Hello, world!” и использовать сборщик Cargo и менеджер пакетов в одном лице.
Глава 2 является практическим введением в язык Rust. В ней объясняются концепции верхнего уровня и в более поздних главах предоставляются дополнительные детали о них. Если хотите сразу погрузиться в практику, то  для этого предназначена глава 2.
Вначале можно даже пропустить главу 3, которая рассказывает про возможности языка аналогичные тем, что есть в других языках и перейти к главе 4, для изучения системы владения в Rust. Однако, если вы дотошный ученик, предпочитающий изучить каждую особенность до перехода к следующей, то можно пропустить главу 2 и перейти сразу к главе 3, возвращаясь к главе 2, если захочется  поработать над проектом и применить полученные знания.

Глава 5 описывает структуры и методы, а глава 6 охватывает перечисления, выражения `match` и конструкции управления потоком `if let`. Вы будете использовать структуры и перечисления для создания пользовательских типов в Rust.

В главе 7 вы узнаете о системе модулей Rust и о правилах конфиденциальности для организации вашего кода и его публичного программного интерфейса - Application Programming Interface (API). В главе 8 обсуждаются некоторые общие коллекции структур данных, которые предоставляет стандартная библиотека, например, векторы, строки и хэш-карты. Глава 9 исследует философию и методы обработки ошибок Rust.

В главе 10 рассматриваются шаблонные типы данных, типажи и времена жизни, которые дают вам силу разрабатывать код, который может использоваться разными типам. 
Глава 11 посвящена тестированию, которое даже с гарантиями безопасности в Rust, необходимо для обеспечения правильной логики вашей программы.
В главе 12 мы создадим собственную реализацию подмножества функциональности инструмента командной строк`grep`, предназначенного для поиска текста в файлах. Для этого мы будем использовать многие концепции, которые обсуждались в предыдущих главах.

Глава 13 исследует замыкания и итераторы: особенности Rust, которые пришли из функциональных языков программирования.
В главе 14 мы подробнее рассмотрим Cargo и расскажем о лучших способах предоставления пользования вашими библиотеками другим разработчикам.
Глава 15 обсуждает умные указатели, которые предоставляет стандартная библиотека и свойства, которые обеспечивают их функциональность.

В главе 16 мы рассмотрим различные модели параллельного программирования и поговорим о том, как Rust помогает вам безбоязненно программировать в нескольких потоках.
Глава 17 рассказывает о том, как идиомы Rust сравниваются с принципами объектно-ориентированного программирования, с которыми вы возможно знакомы.

Глава 18 является справочником по шаблонам и сопоставлению с образцом, которые являются мощным способом выражения идей в программах на Rust.
Глава 19 содержит обзор продвинутых тем, представляющих интерес, включая небезопасный Rust, макросы, больше о временах жизни, шаблонах, типах, функциях и замыканиях.

В главе 20 мы завершим проект, в котором мы реализуем низкоуровневый многопоточный веб-сервер!

Наконец, некоторые приложения содержат полезную информацию о языке в ссылочном формате. Приложение A охватывает ключевые слова Rust, приложение B охватывает операторы и символы Rust, приложение C охватывает выводимые признаки, приложение D содержит инструменты стандартной библиотеки и и приложение E описывает редакции Rust.

Нет способа читать эту книгу неправильно: если вы хотите пропустить что-то и пройти вперёд, делайте это! Возможно, вам придётся вернуться к предыдущим главам, если у вас появятся какие-либо затруднения. Делайте так, как считаете удобным для себя.

<span id="ferris"></span>

Важной частью процесса обучения Rust является изучение того, как читать сообщения об ошибках, которые отображает компилятор: они приведут вас к работающему коду. Мы изучим много примеров, которые не компилируются и отображают ошибки в сообщениях компилятора в разных ситуациях. Знайте, что если вы введёте и запустите случайный пример, он может не скомпилироваться! Убедитесь, что вы прочитали окружающий текст, чтобы понять, не предназначен ли пример, который вы пытаетесь запустить, для демонстрации ошибка. Ferris также поможет вам различить код, который не предназначен для работы:

Ferris | Пояснения
--- | ---
<img src="img/ferris/does_not_compile.svg" class="ferris-explain"> | Этот код не компилируется!
<img src="img/ferris/panics.svg" class="ferris-explain"> | Этот код вызывает состояние "panic"!
<img src="img/ferris/unsafe.svg" class="ferris-explain"> | Этот блок содержит небезопасный код.
<img src="img/ferris/not_desired_behavior.svg" class="ferris-explain"> | Этот код ведёт себя не так, как предполагается.

В большинстве случаев мы приведём вас к правильной версии любого кода, который не компилируется.

## Исходные коды

Файлы с исходным кодом, используемым в этой книге, можно найти на [GitHub] .


[The Rust Programming Language]: https://nostarch.com/rust
[No Starch Press]: https://nostarch.com/
[GitHub]: https://github.com/rust-lang/book/tree/master/src