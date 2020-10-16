# Лабораторна робота №1
## Тема: Дослідження команд RISC та CISC
![alt text](https://habrastorage.org/webt/fk/di/xh/fkdixhljjmeiwzy6vdeb-loeoz0.png)
## Мета: дослідити набори команд RISC та CISC, з’ясувати основні
## Хід роботи
1. Вивчить теоретично набори команд RISC, CISC (обов’язково знаходити додаткові джерела інформації)
2. Заповніть діаграму порівняння за бажанням в неї можливо додати додаткові параметри.
3. Зробіть висновки.
| Основа для порівняння | RISC |CISC|
|-----------------------|------|----|
| Наголос (основа на чому базується) |RISC (англ. Reduced Instruction Set Computing — обчислення зі скороченим набором команд) — архітектура процесорів зі скороченим набором команд. Також відома як «архітектура load-store», позаяк система команд такої архітектури не включає арифметико-логічних операцій з операндами у пам'яті. Для будь-якого оброблення даних їх спочатку слід завантажити (англ. Load) в регістр, виконати необхідні операції, а тоді зберегти (англ. Store) назад у пам'ять. Найвідоміші представники: ARC[en], Alpha, Am29000[en], ARM, AVR, Blackfin[en], i860, i960, M88000[en], MIPS, PA-RISC, Power Architecture[en] (включаючи PowerPC), RISC-V, SuperH[en], та SPARC.  | CISC (англ. Complex instruction set computing або complex instruction set computer) - тип процесорної архітектури, яка характеризується наступним набором властивостей: нефиксированное значення довжини команди; арифметичні дії кодуються в одній команді; невелике число регістрів, кожен з яких виконує строго певну функцію.   |
|Розмір набору інструкцій | Малий| Великий|
| Формати інструкцій | Фіксований (32-бітний) формат|Різні формати (16-64 біт кожної інструкції).|
| Використовуються режими адресації|Обмежено до 3-5|12-24|
| Використовуються регістри загального призначення |32-192|8-24|
| Висновки пам'яті |Зареєструйтеся для реєстрації|Пам'ять в пам'ять|
| Дизайн кешу |Розділити кеш даних і кеш інструкцій.|Єдиний кеш для інструкцій і даних.|
| Тактова частота (типові) |50-150 МГц|33-50 МГц|
| Цикли на інструкцію |Єдиний цикл для всіх інструкцій і середній ІСЦ <1.5.|ІСЦ між 2 і 15.|
| Керування процесором |Обмотка без пам'яті управління.|Мікрокодування з використанням керуючої пам'яті (ПЗУ).|
## Висновки
Інструкції CISC є складними і мають тенденцію до уповільнення, ніж RISC, але використовують менше циклів з меншою кількістю інструкцій.
## Контрольні питання
Коротко охарактеризуйте набір команд RISC?
Набори команд зі зменшеними наборами команд (RISC), як правило, містять менше 100 інструкцій і використовують фіксований формат інструкцій (32 біта). Він використовує кілька простих режимів адресації. Використовуються інструкції на основі реєстру, що означає, що використовується механізм реєстрації для реєстрації. LOAD / STORE - єдині незалежні інструкції для доступу до пам'яті.
Для підвищення швидкості перемикання контекстів використовується великий файл реєстру. Простота наборів команд призвела до реалізації цілих процесорів на одному чіпі VLSI. Додатковими перевагами є більш висока тактова частота, нижчий ІСЦ, що регулюють високі рейтинги MIPS на наявних RISC / суперскалярних процесорах.
Коротко охарактеризуйте набір команд CISC?
Комплекс команд набору команд (CISC) набір інструкцій містить близько 120 до 350 інструкцій. Він використовує змінні формати інструкцій / даних, але невеликий набір регістрів загального призначення, тобто 8-24. Причиною великих наборів команд є використання інструкцій змінного формату. Велика кількість еталонних операцій пам'яті виконується за допомогою величезної кількості режимів адресації.
Архітектура CISC безпосередньо використовує оператори HLL в апаратних / прошивках. Єдиний кеш використовується в традиційній архітектурі CISC, яка містить як дані, так і інструкції, і використовує загальний шлях.
Дайте порівняння цих наборів команд.
- У RISC розмір набору команд невеликий, а в CISC величина набору команд велика.
- RISC використовує фіксований формат (32 біта) і в основному регіональні інструкції, тоді як CISC використовує діапазон змінних форматів від 16-64 біт на інструкцію.
- RISC використовує один годинник і обмежений режим адресації (тобто 3-5). З іншого боку, CISC використовує декілька годин від 24 до 24 режимів адресації.
- Кількість регістрів загального призначення, які використовує RISC, коливається від 32-192. Навпаки, архітектура CISC використовує 8-24 GPR.
- Механізм реєстрації в регістр використовується в RISC з незалежними інструкціями LOAD і STORE. На відміну від цього, CISC використовує механізм пам'яті до пам'яті для виконання операцій, крім того, включені інструкції LOAD і STORE.
- RISC має розділені дані та кеш керування інструкціями. На відміну від цього, CISC використовує уніфікований кеш для даних і інструкцій, хоча останні конструкції також використовують розділені кеші.
- Більшість елементів керування процесором в RISC є провідними без наявності пам'яті керування. І навпаки, CISC мікрокодується і використовує керуючу пам'ять (ROM), але сучасний CISC також використовує жорстке керування.

## Джерела
[1. Вікіпедия—Reduced Instruction Set Computing](https://uk.wikipedia.org/wiki/Reduced_Instruction_Set_Computing)
1. [Вікіпедия—Reduced Instruction Set Computing](https://uk.wikipedia.org/wiki/Reduced_Instruction_Set_Computing)

[2. Вікіпедия—CISC](https://ru.wikipedia.org/wiki/CISC)
2. [Вікіпедия—CISC](https://ru.wikipedia.org/wiki/CISC)

[3. Різниця між RISC і CISC](https://uk.gadget-info.com/difference-between-risc)
3. [Різниця між RISC і CISC](https://uk.gadget-info.com/difference-between-risc)
