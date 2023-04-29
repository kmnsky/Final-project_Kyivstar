![alt text](https://www.topgear.com/sites/default/files/cars-car/image/2015/07/02_01_10mb.jpg)

# Driver segment among subscribers

Архів містить 4 файли

tabular_data.csv, hashed_feature.csv, train.csv, test.csv.

Необхідно побудувати модель, що виявлятиме сегмент водіїв серед абонентів ПрАТ «Київстар».

Це задача бінарної класифікації:
- «1» абонент являється водієм (відноситься до сегменту водіїв),
- «0» абонент не є водієм (не відноситься до сегменту водіїв).

Файли tabular_data.csv і hashed_feature.csv  ̶ тут описові характеристики щодо 4084 абонентів («ID» – це ідентифікатор абонента).

Файл train.csv  ̶ це дані щодо цільової мітки (чи належить абонент до сегменту водіїв).

Файл test.csv  ̶ це список абонентів, для яких необхідно зробити прогноз, за яким ми й будемо оцінювати якість ваших моделей.

## А тепер детальніше

### tabular_data.csv 
Містить числові дані щодо активності абонента за 12 періодів: 

- period – номер періоду (періоди послідовні, 1 – найновіший);
- id – ідентифікатор абонента;
- feature_0 – feature_49 – дані щодо активності абонента у відповідний період.

### hashed_feature.csv 
Тут набір захешованих значень однієї категоріальної змінної для абонента:

- id – ідентифікатор абонента;
- feature_50 – хеш від значення категоріальної змінної.

### train.csv 
Тут дані з цільовою міткою:

- id – ідентифікатор абонента;
- target – значення цільової мітки (1 – належить до сегменту водіїв, 0 – не належить до сегменту водіїв).

### test.csv 
Список абонентів, для яких потрібно зробити передбачення за допомогою ваших моделей:

- id – ідентифікатор абонента;
- score – ймовірність того, що абонент належить до сегменту водіїв (класу «1»). Цю ймовірність визначає ваша модель
