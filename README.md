# SN74HC147N

## Завдання
Завданням було підключити та затестувати Texas Instruments SN74HC147N 10 - 4 пріоритетний енкодер. Він приймає лише MSB з вхідних даних.
Допоміжними засобами був PSoC 4 Pioneer Kit (CY84248LQI-BL583), PSoC Creator v4.4 за софт.

<img width="447" height="403" alt="image" src="https://github.com/user-attachments/assets/15701af9-933e-405b-93c6-4e1f1513a5c6" />

На вхід даються дані через піни 1 - 9. Аутпутами є 4 піни A B C D.

## Тест

<img width="519" height="360" alt="image" src="https://github.com/user-attachments/assets/712adb95-ebc5-4c0c-90b9-80d38982e686" />

Спираючись на таблицю істиності, (Н - logic 1, L - logic 0, X - irrelevant) 

### Результати
Результати виводяться в UART, задля виконання завдання "Засвітити LED" я з'єднав вихідний пін A до LED3 R (Червоний пін на PSoC4, пін 2.6).

<img width="301" height="180" alt="image" src="https://github.com/user-attachments/assets/b758e3c7-3a66-4afe-8678-70fbfc34c2fd" />

*For L on input index 1* - означає, що L задається на індексі 1 (див. таблицю істиності).   

Також варто зазначити, що енкодер повертає бінарне представлення найприорітетніщого біта.
<img width="296" height="148" alt="image" src="https://github.com/user-attachments/assets/a4cb06dd-7f21-4cd7-ab9f-6b2dc074489d" />

**Приклад:** На вхід передаємо 5 (0101), На вихід ми отримуємо 3 (1100, little-endian)


### Додатково

<a href="https://www.datasheet.live/pdfviewer?url=https%3A%2F%2Fpdf.datasheet.live%2F90751103%2Fti.com%2FSN74HC147N.pdf">Даташіт</a>
