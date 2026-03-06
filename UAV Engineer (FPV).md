
1. FPV дрон: огляд архітектури, основних компонент
    - Компоненти
        - рама: конструкція, матеріали, розміри, типи
        - мотори: типи, характеристики
        - політний контролер + ESC: призначення, види, відмінності, можливості
        - радіозв'язок: типи, протоколи, частоти, антени
        - відео: передавачі, потужність, антени, з'єднання
        - управління: види пультів, режими
    - Матеріали
        1. Народний FPV (онлайн, безкоштовний, 8 годин, мова: україніська), https://prometheus.org.ua/prometheus-free/fpv-engineering/
        2. Туторіали Social Drone, https://sdua.tech/request
    - Рекомендація
        - Зібрати кілька бортів самостійно
2. Політний контролер
    1. Загальна архітектура
        1. Сенсори: гіроскоп, акселерометр, барометр, gps, компас
            1. [Акселерометр і гіроскоп](https://www.youtube.com/watch?v=RZd6XDx5VXo)
        2. Інтерфейси і протоколи: I2C, I2C/SPI, UART, IZC, CRSF, MSP
            1. Приймач: CRSF
            2. ESC: DShot
        3. VTX
        4. PID регулятори
        5. Синтез даних і фільтри (Sensor fusion)
            1. [Комплементарний фільтр](https://www.youtube.com/watch?v=BUW2OdAtzBw)
            2. [Розширений фільтр Калмана (Extended Kalman Filter - EKF)](https://www.youtube.com/watch?v=hQUkiC5o0JI)
            3. [Практична реалізація EKF на вбудованих системах (STM32)](https://www.youtube.com/watch?v=7HVPjkWOrLE)
3. Прошивки та екосистеми
    1. Відмінності і переваги різних екосистем
        1. Flight Controller Explained: How to Choose the Best FC for FPV Drone, https://oscarliang.com/flight-controller/
        2. Flight Controller Firmware for FPV Drone: Choosing Between Betaflight, iNav, Ardupilot, https://oscarliang.com/fc-firmware/
    2. Betaflight
        1. PID регулятори
            1. [Налаштування PID регулятора для FPV дронів в Betaflight. Теоретична частина (Aves Lab)](https://www.youtube.com/watch?v=NlqPHb28eaw)
            2. [Практичні поради з налаштування PID регулятора Betaflight для FPV дронів (Aves Lab)](https://www.youtube.com/watch?v=76FeOTWqC_Y)
        2. Фільтри
            1. [Betaflight 4.5 Filter Tuning (Chris Rosser)](https://www.youtube.com/watch?v=E3s5XYk3M74&list=PLFPBjpbd5xKQwhan-h17pKlEyIvE3TlP2)
        3. Налаштування, вирішення проблем
            1. [Blackbox Explorer, аналіз політних логів (Aves Lab)](https://www.youtube.com/watch?v=FhQDbtbXL5Y&t=1s)
            2. [Налаштування 10-дюймового FPV дрона на рамі Mark4 V2](https://www.youtube.com/watch?v=lgfKJPVtjwQ)
    3. iNav
        1. [Налаштування дронів в конфігураторі INAV](https://www.youtube.com/watch?v=xWo17kdRwOE)
        2. [iNav PIDs](https://www.youtube.com/watch?v=xWo17kdRwOE)
    4. Ardupilot
        1. Вступ
            1. [Різниця між ArduPilot та Betaflight, можливості автономних місій та те, які переваги отримує дрон (стабілізація, утримання висоти, робота з датчиками) (Обережно дрони)](https://www.youtube.com/watch?v=e3Sw86PXz24&list=TLGGWoBgJMpS8hsyMjAyMjAyNg)
            2. [Налаштування дрона на ArduPilot:  ПЗ для наземних станцій, сумісність польотних контролерів та процес прошивки через STM32 Cube Programmer](https://www.youtube.com/watch?v=M8G8ju4f7HI)
        2. Налаштування
            1. [Огляд Mission Planner та робота із Full Parameter List](https://www.youtube.com/watch?v=OhRJUr8OFWs)
            2. [Налаштування дрона на ArduPilot. Частина 2 Загальні налаштування дрона в MissionPlanner, вибір типу рами, калібрування акселерометра та компаса, налаштування портів (UART), радіоапаратури та перевірку порядку обертання моторів](https://www.youtube.com/watch?v=XofUf0LPJ8M)
            3. [Hardware and Setup: Complete ArduPilot Tuning Guide (Chris Rosser), з'єднання з ESC, налаштування GPS/компаса, логування та підготовку до першого тестового зависання (hover test)](https://www.youtube.com/watch?v=4pkSnBqA_m4)
        3. Файнтюн
            1. [Ardupilot: налаштовуємо ПІД регулятор і фільтри вручну (FPV питаннячка), ручний тюн PID-регуляторів і фільтрів, аналіз логів, боротьба з вібраціями](https://www.youtube.com/watch?v=XDkSa0SjF7I)
    5. PX4
        1. [PX4 Ultimate Tuning Guide (Chris Rosser), детальний огляд, починаючи з порівняння з Ardupilot](https://www.youtube.com/watch?v=jxqWg7s5jv8&list=PLFPBjpbd5xKRECBsvI3MbmsS8NQJ8l8L9&index=6)
4. Силова установка
    1. Мотори
        1. [KV характеристика моторів (Chris Rosser)](https://www.youtube.com/watch?v=uvyi6hPIt8w)
        2. Контролер обертів (Electronic Speed Controller - ESC)
            1. [Тюнінг BLHeli_32 для запобігання десинхронізації (Chris Rosser)](https://www.youtube.com/watch?v=7WeHTb7aBrE)
            2. [Перехід з BLHeli_32 на AM32 (Chris Rosser)](https://www.youtube.com/watch?v=VCIpMOESqmw)
            3. [Тюнінг AM32 (Chris Rosser)](https://www.youtube.com/watch?v=3SHzyUaypFw)
    2. Пропелери
        1. [Вибір правильних пропелерів (Chris Rosser)](https://youtu.be/epJ6L9MaXOQ?si=JVfNvUKqN2l_i_2v)
    3. Батареї
        1. Типи батарей Li-Ion, Li-Po, LiFePO4
        2. Напруги, струми, ємність, паралельне, послідовне зʼєднання
5. Зв'язок
    1. Радіофізика та антени
        1. Антени: типи поляризацій, характеристики, види
            1. [Будова антени, принцип роботи, безпека (Holy Tarantino)](https://www.youtube.com/watch?v=M0ZpfBoJZ5o)
            2. [Гармоніки та їхній вплив на відеосигнал (Holy Tarantino)](https://www.youtube.com/watch?v=aIqn18uq9E8)
            3. [Показники якості зв'язку (RSSI, LQ, SNR) (Holy Tarantino)](https://www.youtube.com/watch?v=y1gqLveX6Co)
        2. Поляризації, діаграми направленості, зона Френеля, гармоніки, фільтри, параметри фільтрів, діаграма Сміта, LiteVNA
            1. [Діаграми Сміта від W2AEW](https://youtube.com/playlist?list=PL4ZSD4omd_AzQ7T0Dt4zTBW8sHLQHjqMQ&si=tXCA3_fsHPar_TD2)
    2. Протоколи
        1. LoRa (spreading factor, chirp, bandwidth і т.д.)
        2. ELRS
        3. MAVLink
6. Інструменти (софт)
    1. Betaflight Configurator
    2. Mission Planner / QGroundControl
7. Додаткові теми
    1. Теорія управління
        1. [Вступ](https://www.youtube.com/watch?v=oBc_BHxw78s&list=PLUMWjy5jgHK1NC52DXXrriwihVrYZKqjk)
        2. [Курс від Brian Douglas](https://engineeringmedia.com/videos)
