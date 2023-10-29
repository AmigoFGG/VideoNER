__README для кода извлечения тегов с использованием spaCy__
__Описание__
Данный скрипт предназначен для извлечения и добавления тегов (сущностей) к текстовым данным из файла Excel, используя библиотеку spaCy для обработки текста на русском языке. Эти теги представляют собой информацию о сущностях в тексте, такие как даты, бренды, виды спорта и другие. После извлечения, результаты сохраняются в новом файле Excel.

__Зависимости__
Прежде чем использовать этот код, убедитесь, что у вас установлены следующие зависимости:

pandas: Библиотека для работы с данными в формате таблицы.
spaCy: Библиотека для обработки естественного языка.
concurrent.futures.ThreadPoolExecutor: Для выполнения параллельных вычислений.
Также необходимо установить spaCy модель для русского языка, с именем "ru_core_news_sm".

__Использование__
Убедитесь, что у вас есть файл "ner_data_train.xlsx" с данными, которые вы хотите обработать. Если нужно, замените это имя файла на имя вашего собственного файла.
Запустите скрипт. Он выполняет следующие шаги:
Загружает данные из файла "ner_data_train.xlsx".
Определяет теги согласно предоставленным описаниям в словаре tag_descriptions.
Использует spaCy для извлечения тегов из текста.
Параллельно обрабатывает данные с использованием ThreadPoolExecutor для ускорения процесса.
Сохраняет результаты в новом файле Excel с именем "output_processed_with_tags.xlsx".
Выводит обработанные данные в консоль.

__Описание структуры данных__
ner_data_train.xlsx: Файл Excel с исходными данными, которые будут обработаны.
tag_descriptions: Словарь, который описывает различные теги и их описание.
tags_to_extract: Список тегов, которые необходимо извлечь из текста.
nlp: Загруженная spaCy модель для русского языка.
extract_tags(text): Функция, которая извлекает теги из текста.
process_batch(batch): Функция для обработки нескольких строк данных параллельно.
batch_size: Размер пакета данных для параллельной обработки.
batches: Разделение данных на пакеты для параллельной обработки.
processed_batches: Результаты обработки данных в пакетах.
tags_result: Общий список тегов, полученных после обработки.
Результаты сохраняются в файле "output_processed_with_tags.xlsx".
Обработанные данные выводятся в консоль.

__Пример использования__
Для выполнения скрипта, выполните следующую команду:

bash
Copy code
python имя_вашего_скрипта.py
Замечания
Перед запуском убедитесь, что у вас установлены все необходимые зависимости и что файл "ner_data_train.xlsx" с данными существует в текущем каталоге.
Вы можете настроить параметры, такие как размер пакета (batch_size) и количество потоков (max_workers), в зависимости от ваших потребностей.# VideoNER
Код для распознавания сущностей в видео под названием VideoNER
--------------------------------------------------------------
Чтобы запустить его:
1. Создать папку на рабочем столе;
2. Перекинуть туда файл;
3. Перекинуть туда файл (таблица) с тем, с чем будем работать
   
