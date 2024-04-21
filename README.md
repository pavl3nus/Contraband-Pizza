# Contraband-Pizza
Игра из курса Ulearn ОП На C# 2

**Платформа:** Windows<br>
**Технологии:** Monogame<br>
**Язык:** C#<br>
**Жанры:** Аркада, Гонки, Приключения, Экшен<br>
**Сеттинг:** Real Life<br>
**Графика:** Пиксельная<br>
**Музыка:** Синтвейв<br>
**Длительность:** Не более часа<br>

## Сюжет
Вы устраиваетесь на работу доставщика пиццы в небольшом городке с одним лишь условием - не заглядывать в сумку с пиццей. Выполняете несколько заказов. После очередного заказа вы понимаете, что что-то здесь не так, потому что доставка пиццы превращается в полицейскую погоню. Оторвавшись от копов, вы решаете всё-таки заглянуть в сумку. Вы обнаруживаете, что в сумке не что иное, как запрещённые вещества. В конечном итоге Вы решаете разобраться с нанимателем.

## Игровой мир и геймплей
Вид сверху. Город с дорогами и домами. По городу разбросаны 5 уровней по доставке пиццы, каждый из которых представляет собой дорогу с трафиком (автомобилями) и препятствиями-обрывами дороги. Игроку необходимо проехать заданное количество метров не разбившись для прохождения уровня и успешной доставки пиццы клиенту. По дороге разбросаны собираемые усиления. Перед началом каждого уровня игроку поступит звонок, после которого в городе будет отмечена точка старта. В городе играет спокойная музыка, когда как на уровнях играет динамичная композиция, для каждого своя.

### Уровни
1. Простой уровень - минимум трафика, препятствий нет, небольшая скорость, 5 полос движения. В начале уровня будет подсказка по обучению. У игрока есть 5 жизней, то есть 4 раза он может столкнуться с трафиком. Без усилений;
2. На этом уровне будут доступны усиления, так же будет увеличено количество автомобилей на дороге, появятся препятствия, 5 полос движения, 3 жизни;
3. Уровень с одной жизнью и всего тремя полосами движения. Есть только автомобили. Из усилений только замедление. Скорость игрока понемногу увеличивается к концу уровня. В конце уровня появляется полицейская машина, медленно проезжающая мимо игрока;
4. Две жизни, 4 полосы движения, все усиления + генератор ЭМИ. В середине уровня за игроком начинается полицейская погоня. После погони в случае удачного прохождения уровня игрок откроет сумку и увидит, что он перевозит на самом деле;
5. Финальный уровень. Без усилениц. Получателем заказа является наниматель и игроку предстоит уничтожить его. Битва происходит в заброшенном ангаре.

## Объекты и взаимодействие с ними
1. Автомобили трафика. Едут по дороге на уровнях. Иногда перестраиваются в соседнюю полосу, если она не занята. При столкновении игрока с ними он теряет жизнь/погибает. Пока что подразумеваются 8 типов автомобилей (по форме и цвету). При столкновении с препятствием/полицейским автомобилем сворачивают с дороги;
2. Препятствие. Конец дороги или камень. При столкновении с игроком, игрок теряет жизнь/погибает;
3. Полицейский автомобиль. В сущности то же, что и автомобиль трафика, только умеет через константное время таранить игрока сзади. Так же могут ускоряться и таранить игрока сбоку. Восприимчив к ЭМИ. При использовании ЭМИ игроком немедленно останавливаются/сворачивают с дороги;
4. Наниматель. Наниматель хаотично перемещается по комнате и при касании игрока убивает его. Игрок должен всадить 10 пуль из пистолета по нанимателю и тогда игра заканчивается его победой;
5. Усиления. Усиления лежат на дороге, когда игрок наезжает на них, усиление активируется. Виды усилений: ускорение игрока, замедление игрока, прозрачность трафика, генератор ЭМИ для выведения из строя полицейских автомобилей (доступно только на 4-м уровне).
6. Пистолет. Доступен игроку только на последнем уровне при битве с нанимателем. Выстрелить можно раз в 8 секунд.
