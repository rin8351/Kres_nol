## Kres_nol
### Мой вариант игры Крестики нолики.

Для включения необходимо вызвать метод menu объекта класса krest.

### 1. Выбор в методе menu   
1.1. Игра с компьютером:   
1.1.1. комп ходит рандомно   
1.1.2. комп выбирает стратегию (см. пункт Стратегия компа)   
1.2. Выбор очередности, кто ходит первмы- компьютер или игрок   
1.3. просмотр заданного количества игр двух компьютеров   
1.3.1. когда оба компьютера ходят рандомно   
1.3.2.... в соответствии с выбранной стратегией   

### 2. Общие сведения   
2.1. 1-ый компьютер в качестве своего хода выставляет цифру 1 на поле . 2-ой компьютер или игрок- цифру 2. Пустые клетки обозначены цифрой 0.   
2.2. При инициализации любого вида игры методом variation заполняются массивы (pob1_var и pob2_var) всех возможных выигрышных позиций отдельно для игрока и компьютера.   
2.3. В каждом виде игры после каждого хода включается метод proverka, который проверяет, есть ли на поле выигрышные комбинации игрока и пустые поля (цифра 0).   
Если есть выигрышная комбинация- игра заканчивается, ходы прекращаются, засчитывается победа. Если на поле нет пустых клеток (цифры 0)- игра заканчивается, засчитывается Ничья.   
Выигрышная комбинация это 3 цифры игрока (1 или 2) в одном из вариантов последовательностей: одна из двух диагоналей, одна из трех строк, один из трёх столбцов.   
2.4. Под стратегией понимается выигрышная позиция из трех цифр, которую компьютер выполняет каждый ход, пока что нибудь не помешает ее осуществлять (второй игрок, победа, Ничья)

### 3. Ходы компьютера   
3.1. Рандомный ход.   
Компьютер выбирает любую клетку равную нулю, пока такая на поле присутствует.    
3.2. Выбор стратегии   
Каждый ход компьютер делает проверки и делает ход в зависимости от того, какое из нижеуказанных условий первым будет соблюдено:   
3.2.1 если победа (выигрышная комбинация из трех цифр) будет одержана одним следующим ходом   
3.2.2. если соперник победит следущим ходом, то на его пути ставится свой ход   
3.2.3. если вариантов для победы больше нет (приближение к Ничьей), комп ходит рандомно   
3.2.4. если варианты есть, но стратегия еще не выбрана:   
3.2.4.1. стратегия в первую очередь выбирается та, в соответствии с которой на поле уже стоят свои цифры   
3.2.4.2. в противном случае выбирается стратегия рандомно   
3.2.5. если стратегия уже выбрана, компьютер продолжает ставить свои ходы в соответствии с ней   
