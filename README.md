# "Зеленая перепись"
  
**Команда "Извилинки":**  
- Елизавета Кубанкова (капитан)  
- Кирилл Шмелёв  
- Дарья Кашина  
- Виктория Страхова  
- Настасья Богуш  

**Постановщик кейса:** Департамент природопользования и охраны окружающей среды города Москвы  
  
## Задача  

    
Разработка концепции единой системы мониторинга и учёта городских зелёных насаждений г. Москвы

<details><summary><b>Описание решения</b></summary>   

Мы разработали концепцию системы мониторинга и учёта городских зелёных насаждений. До разработки концепции был проведен конкурентный анализ существующих систем, который позволил предложить наиболее актуальное решение и учесть мировой опыт решения проблемы инвентаризации растений.  

Мы предлагаем использовать уже существующие технологии сбора данных об озелененных территориях с помощью геоснимков, дронов и лидаров, в зависимости от типа территорий, доступности, требований к детализации и других ограничений. Хранение снимков в БД и объектных хранилищах позволит непрерывно актуализировать информацию. Обработка снимков с помощью машинного обучения позволит быстро и качественно определить площадь озеленения, растительный состав районов и другие метаданные, необходимые для качественной и автоматизированной паспортизации территорий. Кроме этого предлагаем рассмотреть варианты оптимизации и упрощения форм паспортов зеленых насаждений.

Уникальность идеи состоит в автоматизации рутинных процессов, а также улучшении пользовательского опыта: для анализа данных и их использования в управленческих целях предлагается создать информативные дашборды (анализ, мониторинг состояния, своевременное реагирование) и интерактивную карту зеленых насаждений. Также привлекаем жителей города путем развития социальных и развлекательных программ, так как они тоже могут фотографировать участки озелененной территории и отправлять данные в Министерство природопользования, а также влиять на озеленение или очистку тех или иных территорий.

Нами разработана дорожная карта реализации проекта на два года, составлено экономическое обоснование, описано техническое решение, а также предложены способы взаимодействия с жителями города.
Успешная реализация проекта в перспективе позволит масштабировать проект в рамках страны для использования данной системы в других городах России.

**Срок реализации: 2026 г.**

**Стоимость: 100 млн.руб.**

</details> 

<details><summary><b>Конкурентный анализ</b></summary>   

  
Перед разработкой концепции системы учета мы провели конкурентный анализ, чтобы понимать, какие системы учета и мониторинга уже существуют на рынке, каким функционалом они обладают, какие видны тенденции и в какую сторону мы можем развивать наш проект.   
  
1) При проведении конкурентного анализа рассмотрены решения в странах Южной Америки, США и некоторых объектов РФ 
2) Типы существующих решений : GIS, облачные хранилища, мобильные приложения. Решений, основанных на спутниковых системах слежения очень мало, как и WEB. 
3) Функции существующих решений:  
* Учет и анализ зеленых насаждений
* Автоматизация учета и мониторинга
* Экологический мониторинг и оценка состояния экосистемы
* Управление городским хозяйством с учетом озеленения
* Инструменты для оценки экосистемных услуг
4) Данные, получаемые из существующих систем учета:
* Данные о состоянии деревьев и кустарников
* Информация о работах по обслуживанию зеленых насаждений
* Экосистемные услуги (поглощение углерода, качество воздуха)
* Инвентаризация и оценка здоровья растений.
5) Чего не хватает в существующих системах:  
* Недостаток семейного контента: системы ориентированы на профессионалов, что ограничивает вовлечение семей и широкой аудитории
* Низкая известность: недостаточная известность за пределами профессиональных кругов мешает внедрению на местном уровне
* Отсутствие интерактивности: нет игровых элементов, которые могли бы сделать процесс учёта и мониторинга увлекательным


</details>  

<details><summary><b>Концепция</b></summary>   

1) Оптимизация текущей паспортизации  
2) Получение снимков при помощи различных устройств (геоснимки, дроны, лидары, фотографии жителей) в зависимости от типа территории, ограничений (бесполетные зоны, непроходимая местность, заброшенные зоны, режимные объекты и так далее) и их обработка при помощи ML-моделей. Унификация форматов полученных снимков  
3) Хранение данных в единой БД, верификация данных (в том числе проверка дублирования информации) с использованием автоматизированных ML-подходов, а также ручной проверки в спорных случаях  
4) Использование методов CV* для определения типов зеленых насаждений, их состояния и других особенностей территорий  
5) ГИС-системы или WEB-приложения в качестве пользовательского интерфейса. Интерактивная карта зеленых насаждений.  
6) Сбор обратной связи от жителей г. Москвы при помощи простых форм  
7) Вовлечение жителей и гостей столицы в процессы озеленения путем социальных 
и развлекательных программ и активностей
  
</details>  

<details><summary><b>Техническая часть</b></summary>    

### Технологии для сбора данных об озелененных территориях

1. Геоспутниковые снимки

**Преимущества:**  
* Широкий охват. Спутники могут покрывать большие площади, что сокращает время на сбор данных  
* Регулярность обновлений. Возможность получения данных с высокой частотой обновления  
  
**Примеры аппаратов:**  
*Sentinel-2 (ESA):* Предоставляет бесплатные данные с высоким пространственным разрешением (10 м)  
*Landsat (NASA/USGS):* Обеспечивает многолетние данные для исторического анализа  
  
2. Снимки с дронов  
  
**Преимущества:**  
* Высокое разрешение. Возможность получения изображений с высоким уровнем детализации
* Гибкость. Дроны могут запустить в любое время и на конкретных участках, где требуется более детальное изучение
  
**Примеры аппаратов:**  
*DJI Phantom 4 RTK:* Используется для картографирования и создания 3D-моделей местности  
*senseFly eBee X:* Подходит для крупных проектов, высокое разрешение и долгий полет  

4. Лидар (LiDAR)
  
**Преимущества:**  
* Точность. Высокая точность в измерении высоты и создания 3D-моделей
* Сканирование растительности. Позволяет «видеть» сквозь листву и получать данные о подлеске
  
**Примеры аппаратов:**  
*Velodyne HDL-32E:* Подходит для установки на дроны или автомобили для сбора данных в городской среде  
*RIEGL VUX-1:* Используется для высокоточного картографирования с воздуха  

6. Геодезические приборы (для верификации данных, полученных со снимков)
    
**Преимущества:**  
* Высокая точность на небольших участках. Позволяют проводить детальные замеры на местности  
* Подходят для верификации данных, полученных другими методами
   
**Примеры аппаратов:**   
*Trimble R10:* GNSS-приемник для высокоточных измерений  
*Leica Total Station:* Используется для съемки точек и измерения расстояний с высокой точностью  
  
Предлагаем использовать сочетание этих технологий для получения точных и актуальных данных. Например, спутниковые снимки для общего охвата территории и дроны с Lidar для детального изучения отдельных участков.  

### Хранение и обработка снимков  

**1) База данных**  
Используем потенциально масштабируемую базу данных, такую как *PostgreSQL* с расширением *PostGIS* для хранения геопространственных данных. Это позволит эффективно управлять данными о местоположении и выполнять пространственные запросы  
  
**2) Объектное хранилище**  
*Amazon S3* или аналогичный сервис для хранения больших объемов сырых снимков, полученных с геоспутников, дронов и лидаров  

### Предобработка данных  

**1) Форматы данных**  
Снимки преобразуются в стандартные форматы (например, GeoTIFF для спутниковых данных, LAS для данных лидаров)  

**2) Калибровка данных**   
Коррекция радиометрии и геометрии для исправления потенциальных ошибок в данных, вызванных сенсорами или атмосферными условиями  

## Обработка изображений  

**Сегментация**  
Используем *DeepLab (Tensorflow)* или *U-Net* для сегментации изображения, чтобы отделить озелененные территории от других объектов.
Для определения элементов озеленения обучаем модель на датасете с метками деревьев, кустарников и других посадок.  

**Обнаружение объектов**  
Используем модели типа YOLO или Faster R-CNN для распознавания зданий, сооружений и малых архитектурных форм.  
Модели дообучаем на Google Open Images Dataset или других доступных наборах данных с изображениями и метками элементов благоустройства.  

### Постпроцессинг и расчет метрик  

1) **Кадастровые координаты и схемы расположения**  
Геопривязка результатов с использованием ранее загруженных метаданных и слоев GIS. Определение границ для построения контуров озелененных территорий  
  
2) **Вычисление площадей (функции PostGIS, например ST_Area())**  
  
3) **Анализ дорожной сети и сооружений**  
Используем CV и анализ графов на данных дорожной инфраструктуры для выявления дорожной сети. Для плоскостных сооружений и зданий - выделение контуров и подсчет площади.

### Детальный анализ  

1) Применение ML-алгоритмов для распознавания и классификации элементов насаждений по высоте и форме
2) Используем данные лидара для создания 3D-моделей, позволяющих анализировать рельеф и выявлять малые архитектурные формы.
3) Модели классификации для идентификации видов растений и формирования таблицы насаждений.
4) Отслеживание изменений: сравнение текущих данных с историческими, для выявления изменений в благоустройстве и проведенных ремонтных работах.

### Интерфейс пользователя  

**ГИС-системы или WEB-приложения**  
  
Разработка пользовательского интерфейса, который выводит результаты анализа на карте и позволяет пользователям выполнять интерактивные запросы. Открытые решения, такие как QGIS, могут быть расширены с помощью плагинов для визуализации данных.  
  
Интерфейс должен быть доступен для пользователей с ограниченными возможностями (с поддержкой экранных считывателей).  
  
</details>  

<details><summary><b>Экономическое обоснование решения</b></summary>   

Мы провели подробный расчет трудовых затрат на реализацию проекта длительностью 2 года. За среднюю заработную плату принято значение 1300 р/ч. Суммарно по всем этапам фонд оплаты труда составляет 16,8 млн руб.

Также следует учитывать другие статьи расходы, которые также должны быть учитаны в бюджете проекта. Такие статьи как:  
1) Дополнительные выплаты и социальные взносы
2) Технические расходы:  
* Покупка или аренда серверов и других аппаратных средств  
* Закупка необходимых программных решений и лицензий  
* Обслуживание и техническая поддержка оборудования
3) Разработка и интеграция:
* Затраты на программирование и разработку программного обеспечения  
* Интеграция системы с существующими городскими информационными системами
4) Исследования и анализ:  
* Проведение предварительных исследований и анализа  
* Карты, датчики и другие инструменты для сбора данных
5) Маркетинг и продвижение:
* Продвижение проекта среди жителей и заинтересованных сторон  
* Создание материалов для обучения пользователей
6) Обучение персонала:
* Проведение тренингов и семинаров для сотрудников и пользователей системы
7) Административные расходы:  
* Офисные затраты (аренда, коммунальные услуги)  
* Канцелярские товары и другие текущие расходы
8) Юридические и консультативные услуги:
* Консультации по правовым вопросам  
* Консультации по управлению проектами и внедрению
9) Контроль и мониторинг:
* Система сбора и анализа данных для оценки эффективности
10) Оборудование для машинного обучения (закупка и аренда):  
* Серверы и вычислительные мощности  
* Программное обеспечение
11) Оборудование для съёмки и мониторинга (закупка, аренда, разработка):
* Дроны  
* Лидары  
* Камеры и сенсоры  
12) Обслуживание техники, ремонт, сертификация и страховка  
   
Действительный бюджет проекта требует детального просчета, по нашей предварительной оценке на проект потребуется от 100 млн руб.  


</details> 

## Содержание репозитория  
