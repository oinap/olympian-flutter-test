# Тестовое задание на позицию Flutter-разработчика
## Решение основного задания:
расширил WordItem, чтобы он принимал дополнительный параметр bool shouldShowLottie.
В AreaScreen определяется, является ли WordItem первым словом первого уровня, и передается shouldShowLottie соответственно.
Используем этот флаг внутри WordItem вместе с word.state для условной Lottie анимации.

Плюсы:

Минимальные изменения в существующей архитектуре.
Локализует логику, связанную с Lottie, в WordItem, что делает ее потенциально пригодной для повторного использования.

Минусы:

Логика, определяющая, какой WordItem должен показывать анимацию, должна управляться извне.

## Решение дополнительного задания:

1. Можно использовать batch state updates, чтобы повысить производительность.
2. часто используемые list по которым идет поиск, можно заменить на maps или sets для производительности
3. Централизация ссылок на активы:
 Прямой ввод path к assets может привести к ошибкам, если имена файлов изменятся. Создайте специальный класс для управления path, что повысит удобство обслуживания.

# Задание
Это тестовое задание на вакансию ведущего Flutter разработчика в компанию One Clue. У вас должен быть практический опыт разработки приложений. В этой задаче я ожидаю умение погружаться в существующий проект, реализовывать новую логику в существующем приложения и формулировать свои мыли и решения в текстовом виде.
Для разработки обязательно иметь установленный эмулятор iOS либо реальное устройство.

## Задача
Необходимо добавить анимацию на игровое поле. Анимация должна отображаться до того момента как слово угадают.
[Screen как должно выглядеть](https://github.com/imakarov/olympian-flutter-test/blob/master/test-flutter.png)

## Что сделать:
1. Развернуть приложение на локальном окружении, запустить на ios в эмуляторе или реальном устройстве. После установке при нажатии на кнопку Play вы должны оказаться на экране с 3мя дощечками.

2. Добавить lottie анимацию на экран как показано на изобажении выше (см. Задача). Данная анимация должна появляться только на первом уровне и только на левой верхней дощечке. После того как пользователь отагадает первое слово ("камень", слово может меняться) анимация отображаться не должна.

3. Обосновать свое решение в текстовом виде, положительные и отрицательные моменты реализации на ваш взгляд. Закоммитить в корневой Readme.


## Дополнительное задание (опционально):
Сформулиромать в текстовом виде 3 предложения по рефакторингу чтобы вы хотели изменить в приложении, и обоснование почему считаете что это необходимо сделать. Закоммитить в Readme.

## Как выполнять?
1. Вы можете форкнуть этот репозиторий или клонировать к себе его код
2. После выполнения задания отправляйте ссылку на ваш репозиторий в телеграм [@makarovilya](https://t.me/makarovilya) 

## Ссылки:
1. [Lottie Animation](https://raw.githubusercontent.com/imakarov/olympian-flutter-test/master/Animation.json)
2. [Preview Lottie Animation](https://app.lottiefiles.com/preview)
3. [GitHub](https://github.com/imakarov/olympian_flutter_test)