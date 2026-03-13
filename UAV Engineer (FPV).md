# Навчальні матеріали для інженерів БПЛА

Цей документ — точка входу в інженерію БПЛА для досвідчених розробників ПЗ, які хочуть перейти в оборонну сферу.

Тут зібрані матеріали, які допоможуть розібратись у базових принципах, компонентах і технологіях FPV дронів. Далі вже можна обрати більш вузький напрям: автономність, embedded програмування, звʼязок, digital signal processing, робота з прошивками FC — у defence домені безмежне поле для спеціалізації.

> ⚠️ Список поступово доповнюється.

## Вступ. Анатомія БПЛА і основні компоненти.

1. Огляд архітектури FPV дрона
    1. [Анатомія дрона. З чого зроблений FPV коптер.](https://www.youtube.com/watch?v=hLtEWlq-7uY)
    1. [Базові поняття про FPV дрони та обладнання. Терміни + пояснення.](https://www.youtube.com/watch?v=sfohRjv3Fyk)
1. Навчальні курси і матеріали по збірці FPV дронів:
    1. [Народний FPV](https://prometheus.org.ua/prometheus-free/fpv-engineering/) (онлайн, безкоштовний, 8 годин, мова: україніська)
    1. [Відеоінструкції по збірці FPV дрона від Є-дрон](https://www.youtube.com/watch?v=75SbiwqW7DM&list=PL2Lub8Hfba5QwieEn2fjwiQ--1qiDUZjf)
    1. [Туторіали Social Drone](https://sdua.tech/request)

- **Рекомендація**:
    - Зберіть хоча б пару FPV дронів самостійно і задонатьте на Social Drone або Victory Drones. Це буде найкраще ваше знайомство з цією сферою. В якості бонуса можливо зібраний саме вами дрон знищить якогось окупанта.

## Прошивки польотних контролерів та екосистеми

1. Відмінності і переваги різних екосистем
    1. [Flight Controller Firmware for FPV Drone: Choosing Between Betaflight, iNav, Ardupilot (Oscar Liang)](https://oscarliang.com/fc-firmware/)
    1. [Ardupilot vs Betaflight and INAV (FPV University)](https://www.youtube.com/watch?v=s-xxiiP7oik)
1. Betaflight
    1. Filters and PIDs tuning by Chris Rosser:
        1. [Betaflight 4.5 Filter Tuning (Chris Rosser)](https://www.youtube.com/watch?v=E3s5XYk3M74)
        1. [Betaflight 4.5 PID Tuning (Chris Rosser)](https://www.youtube.com/watch?v=1oYoVE4xu1U)
        1. [Betaflight 4.5 Rates Tuning (Chris Rosser)](https://www.youtube.com/watch?v=P9frW81C31Q)
    1. Налаштування PID регулятора в BetaFlight від Aves Lab:
        1. [Налаштування PID регулятора для FPV дронів в Betaflight. Теоретична частина (Aves Lab)](https://www.youtube.com/watch?v=NlqPHb28eaw)
        1. [Практичні поради з налаштування PID регулятора Betaflight для FPV дронів (Aves Lab)](https://www.youtube.com/watch?v=76FeOTWqC_Y)
        1. [Blackbox Explorer, аналіз польотних логів (Aves Lab)](https://www.youtube.com/watch?v=FhQDbtbXL5Y&t=1s)
    1. Додаткові матеріали по Betaflight:
        1. [Improve your Betaflight Tune w PIDtoolbox](https://www.youtube.com/watch?v=ehvQm8Rqrzk)
        1. [Налаштування 10-дюймового FPV дрона на рамі Mark4 V2](https://www.youtube.com/watch?v=lgfKJPVtjwQ)
        1. [What causes Propwash and how Betaflight Dynamic Idle can help!](https://www.youtube.com/watch?v=CAMcRbQh3xM)
1. Ardupilot
    1. [Плейліст від Criss Rosser](https://www.youtube.com/watch?v=4pkSnBqA_m4&list=PLFPBjpbd5xKSGFJfuQJBPWOm-sGv0VxD1)
    1. [База по ARDUPILOT. Від прошивки до польоту (Є-дрон)](https://www.youtube.com/watch?v=y7PwAig7BhE)
    1. [Плейліст від каналу Обережно дрони](https://www.youtube.com/watch?v=e3Sw86PXz24&list=PLurWqQaDNkG_uVhYsNSvD5VgIOgXVhc2E)
    1. [Ardupilot: налаштовуємо ПІД регулятор і фільтри вручну (FPV питаннячка)](https://www.youtube.com/watch?v=XDkSa0SjF7I)
    1. [QuickTune: 600 строк налаштовують ПІД регулятор (FPV питаннячка)](https://www.youtube.com/watch?v=rLq3naIUMSY)
    1. [ArduPilot SILT with Gazebo playlist (Intelligent Quads)](https://www.youtube.com/watch?v=AP1UC0DlIrE&list=PLy9nLDKxDN683GqAiJ4IVLquYBod_2oA6)
1. iNav
    1. [Налаштування дронів в конфігураторі INAV (Aves Lab)](https://www.youtube.com/watch?v=xWo17kdRwOE)
    1. [INAV Explained playlist (UAV Tech)](https://www.youtube.com/watch?v=mTIcGJwofAg&list=PLcYNkvInloJGvCFbkRoQVkzhyLmdgW_d1)
1. PX4
    1. [PX4 Ultimate Tuning Guide (Chris Rosser), детальний огляд, починаючи з порівняння з Ardupilot](https://www.youtube.com/watch?v=jxqWg7s5jv8&list=PLFPBjpbd5xKRECBsvI3MbmsS8NQJ8l8L9&index=6)

## Компоненти БПЛА

1. Польотний контролер
    1. [Flight Controller Explained: How to Choose the Best FC for FPV Drone](https://oscarliang.com/flight-controller/)
1. Контролер обертів (Electronic Speed Controller - ESC)
    1. [Tuning your BLHeli_32 ESC (Chris Rosser)](https://www.youtube.com/watch?v=7WeHTb7aBrE)
    1. [AM32's NEW configurator settings 100% Explained (Chris Rosser)](https://www.youtube.com/watch?v=VCIpMOESqmw)
    1. [Tuning AM32 ESCs for Ultimate Performance (Chris Rosser)](https://www.youtube.com/watch?v=3SHzyUaypFw)
    1. [Stop Killing ESCs: The Ultimate Capacitor Buying Guide (Chris Rosser)](https://www.youtube.com/watch?v=ANq7a2S0Gik)
1. Мотори
    1. [How to pick the best motor for your quadcopter, now with PHYSICS! (Chris Rosser)](https://www.youtube.com/watch?v=RXy00orSpfU)
    1. [Motor KV 100% Explained (Chris Rosser)](https://www.youtube.com/watch?v=uvyi6hPIt8w)
1. Пропелери
    1. [How to choose the right props for your quadcopter (Chris Rosser)](https://youtu.be/epJ6L9MaXOQ?si=JVfNvUKqN2l_i_2v)
    1. [Prop Direction. Should you run Props IN or Props OUT? (Chris Rosser)](https://www.youtube.com/watch?v=ExFWmOx6yVA)
1. Батареї
    1. [Енергоефективність польоту: як розуміти показники батареї на osd і як та для чого їх враховувати](https://www.youtube.com/watch?v=XcTLhVeCPUc)
    1. TODO: Типи батарей Li-Ion, Li-Po, LiFePO4
    1. TODO: Напруги, струми, ємність, паралельне, послідовне зʼєднання
1. Рами
    1. [Carbon Fibre: A deep dive on this incredible composite material](https://www.youtube.com/watch?v=zXd9wGuDGWI)

## Зв'язок

1. [Показники якості зв'язку (RSSI, LQ, SNR) (Holy Tarantino)](https://www.youtube.com/watch?v=y1gqLveX6Co)
1. [Плейліст по антенах від Holy Tarantino](https://www.youtube.com/watch?v=M0ZpfBoJZ5o&list=PLXQEOJJpWfg6tsT9-SUevw9EwnDXBc5Yy)
1. [The Ultimate Guide to Choosing and Using FPV Antennas](https://oscarliang.com/best-fpv-antenna/)
1. [Інструкція LiteVNA 64. Замір КСХ антени, затухання в кабелі (A-radio)](https://www.youtube.com/watch?v=Vpn25p60xQs)
1. [Гармоніки та їхній вплив на відеосигнал (Holy Tarantino)](https://www.youtube.com/watch?v=aIqn18uq9E8)
1. TODO: Поляризації, діаграми направленості, зона Френеля, гармоніки, фільтри, параметри фільтрів, діаграма Сміта, LiteVNA
1. LoRa:
    1. [LoRa Explained: How It Differs from LoRaWAN (FPV University)](https://www.youtube.com/watch?v=CweHMNx46qQ)
    1. [How LoRa Modulation really works (Visual Electric)](https://www.youtube.com/watch?v=jHWepP1ZWTk)
    1. [LoRa CHIRP (Richard Wenner)](https://www.youtube.com/watch?v=dxYY097QNs0)
    1. [LoRa/LoRaWAN tutorials by Mobilefish.com](https://www.youtube.com/watch?v=cUhAyyzlv2o&list=PLmL13yqb6OxdeOi97EvI8QeO8o-PqeQ0g)
1. Протоколи
    1. [MAVLink](https://mavlink.io/)
    1. [ExpressLRS (ELRS)](https://www.expresslrs.org/)
    1. TODO: CRSF

1. TODO: phased arrays & digital beam forming

## Sensors, sensor fusion, Kalman Filters

1. [Accelerometers and Gyroscopes - Sensor Fusion #1](https://www.youtube.com/watch?v=RZd6XDx5VXo)
1. [Complementary Filter - Sensor Fusion #2](https://www.youtube.com/watch?v=BUW2OdAtzBw)
1. [Extended Kalman Filter - Sensor Fusion #3](https://www.youtube.com/watch?v=hQUkiC5o0JI)
1. [Extended Kalman Filter Software Implementation - Sensor Fusion #4](https://www.youtube.com/watch?v=7HVPjkWOrLE)
1. TODO: add videos by Brian Douglas

## TODO: Control Theory

## Додаткові теми

1. [Classical Control Theory (Brian Douglas)](https://www.youtube.com/watch?v=oBc_BHxw78s&list=PLUMWjy5jgHK1NC52DXXrriwihVrYZKqjk)
1. [All courses from Brian Douglas](https://engineeringmedia.com/videos)
1. TODO: Radar basics
1. TODO: Digital Signal Processing

## Тематичні спільноти

- [Social Drone UA](https://sdua.tech/request)
- [Victory Drones (Discord)](https://www.victory-drones.com/discord)
- [Scream Industries](https://t.me/Scream_Industries_bot)

## Тематичні YouTube канали

- [Є-Дрон](https://www.youtube.com/@E-Drone)
- [Chris Rosser](https://www.youtube.com/@ChrisRosser)
- [UAV Tech](https://www.youtube.com/@uavtech)
- [Holy Tarantino](https://www.youtube.com/@holytarantino)
- [FPV питаннячка](https://www.youtube.com/@FPV-questions)
- [Aves Lab](https://www.youtube.com/@AvesLab)
- [Joshua Bardwell](https://www.youtube.com/@JoshuaBardwell)

## Тематичні Телеграм-канали

- [Сергій FLASH | Про технології](https://t.me/serhii_flash)
- [VD:Розвідка Ворога](https://t.me/VictoryDrones)

## Платні курси

- [Курс Embedded Development (Beetroot Academy)](https://beetroot.academy/courses/online/kurs-embedded-development)
- [Курс Drones Firmware (Beetroot Academy)](https://beetroot.academy/courses/online/kurs-drones-firmware)
