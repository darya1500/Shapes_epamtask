# Shapes

### Индивидуальное задание
#### Куб.
Разработать классы [Точка](https://github.com/darya1500/epam_training/blob/master/src/main/java/by/epam/learn/daryatarasevich/shapes/cube/entity/Point) и [Куб](https://github.com/darya1500/epam_training/blob/master/src/main/java/by/epam/learn/daryatarasevich/shapes/cube/entity/Cube). Создать методы и тесты: [вычисления площади поверхности куба](https://github.com/darya1500/epam_training/blob/master/src/main/java/by/epam/learn/daryatarasevich/shapes/cube/action/CubeAction),
[объема куба](https://github.com/darya1500/epam_training/blob/master/src/main/java/by/epam/learn/daryatarasevich/shapes/cube/action/CubeAction); [соотношения объемов получаемых в результате рассечения куба координатной плоскостью](https://github.com/darya1500/epam_training/blob/master/src/main/java/by/epam/learn/daryatarasevich/shapes/cube/action/CubeAction);
[является ли объект кубом](https://github.com/darya1500/epam_training/blob/master/src/main/java/by/epam/learn/daryatarasevich/shapes/cube/action/CubeAction); [находится ли основание куба на одной из координатных плоскостей](https://github.com/darya1500/epam_training/blob/master/src/main/java/by/epam/learn/daryatarasevich/shapes/cube/action/CubeAction).

#### Task Shapes Chapter A
+ Разработать
[entity](https://github.com/darya1500/epam_training/tree/master/src/main/java/by/epam/learn/daryatarasevich/shapes/cube/entity) классы
+ Entity-классы не следует наполнять методами, выполняющими функциональные действия (методами бизнес-логики, 
такими как вычисление, поиск и т.д.).
+ Разработать [action](https://github.com/darya1500/epam_training/tree/master/src/main/java/by/epam/learn/daryatarasevich/shapes/cube/action)-классы реализующие заданные функциональности, например: «[Реализовать методы вычисления 
площади и периметра круга](https://github.com/darya1500/epam_training/blob/master/src/main/java/by/epam/learn/daryatarasevich/shapes/cube/action/CubeAction)»
+ Параметры, необходимые для создания объектов, организовать как [чтение информации из файла](https://github.com/darya1500/epam_training/blob/master/src/main/java/by/epam/learn/daryatarasevich/shapes/cube/reader/DataReader) [(.txt)](https://github.com/darya1500/epam_training/blob/master/testdata/datafortest.txt). Часть 
данных должны некорректной. Если встретилась некорректная строка, приложение должно переходить к следующей 
строке. Все файлы должны находиться в отдельном каталоге.
+ Для чтения из файла использовать только методы, появившиеся в Java8.
+ Разработать [validation](https://github.com/darya1500/epam_training/tree/master/src/main/java/by/epam/learn/daryatarasevich/shapes/cube/validation)-классы для [проверки результатов вычислений параметров фигур](https://github.com/darya1500/epam_training/blob/master/src/main/java/by/epam/learn/daryatarasevich/shapes/cube/validation/Validator), а также для [валидации 
исходных данных для создания объектов entity-классов](https://github.com/darya1500/epam_training/blob/master/src/main/java/by/epam/learn/daryatarasevich/shapes/cube/validation/DataReaderOutputValidator).
+ Для классов-сущностей следует переопределять методы класса Object: toString(), equals(), hashCode(). Методы класса
Objects не использовать.
+ При решении задачи для создания entity-классов можно использовать паттерн Factory Method.
+ Все классы приложения должны быть структурированы по пакетам.
+ Использовать [собственные классы исключительных ситуаций](https://github.com/darya1500/epam_training/tree/master/src/main/java/by/epam/learn/daryatarasevich/shapes/cube/exception).
+ Оформление кода должно соответствовать Java Code Convention.
+ Для записи логов использовать Log4J2.
+ Код должен быть покрыт Unit-[тестами](https://github.com/darya1500/epam_training/tree/master/src/test/java/by/epam/learn/daryatarasevich/shapes/cube). Использовать TestNG. При написании тестов запрещено: создавать неаннотированные
методы, писать логи и использовать операторы ветвления: if, for, while, do\while, switch; использовать в тест-методе более одного Assert-метода.
+ Класс с методом main в задании должен отсутствовать. Запуск только тестами.

#### Task Shapes Chapter B
+ Площади, Объемы, Периметры фигур должны храниться в объекте класса-[Warehouse](https://github.com/darya1500/epam_training/blob/master/src/main/java/by/epam/learn/daryatarasevich/shapes/cube/warehouse/Warehouse).
+ Любое изменение параметра фигуры должно вызывать [пересчет соответствующих значений в классе- Warehouse](https://github.com/darya1500/epam_training/blob/master/src/main/java/by/epam/learn/daryatarasevich/shapes/cube/observer/ShapeObserver).
Для решения данной задачи использовать паттерны [Observer](https://github.com/darya1500/epam_training/tree/master/src/main/java/by/epam/learn/daryatarasevich/shapes/cube/observer) (можно использовать Flow API) и Singleton 
(потокобезопасные варианты использовать запрещено).
+ Все созданные объекты геометрических фигур сохранить в объекте-репозитории.
+ Используя шаблон [Repository](https://github.com/darya1500/epam_training/tree/master/src/main/java/by/epam/learn/daryatarasevich/shapes/cube/repository), [разработать спецификации по добавлению, удалению и изменению объектов репозитория](https://github.com/darya1500/epam_training/blob/master/src/main/java/by/epam/learn/daryatarasevich/shapes/cube/repository/ShapeRepository).
+ Разработать спецификации по поиску объектов и групп объектов в репозитории. По [ID](https://github.com/darya1500/epam_training/blob/master/src/main/java/by/epam/learn/daryatarasevich/shapes/cube/specification/ByIdSpecification), [по имени](https://github.com/darya1500/epam_training/blob/master/src/main/java/by/epam/learn/daryatarasevich/shapes/cube/specification/ByNameSpecification), по координатам
(например: [найти все объекты точки которых находятся в первом квадранте](https://github.com/darya1500/epam_training/blob/master/src/main/java/by/epam/learn/daryatarasevich/shapes/cube/specification/ByLocationInFirstQuadrantSpecification), [найти все объекты площади поверхности 
(объемы, периметры) которых заключены в заданный диапазон](https://github.com/darya1500/epam_training/blob/master/src/main/java/by/epam/learn/daryatarasevich/shapes/cube/specification/ByRangeAreaLessThanHundredSpecification), найти объекты находящиеся на расстоянии в заданном диапазоне от 
начала координат)
+ Разработать методы сортировки наборов объектов по [ID](https://github.com/darya1500/epam_training/blob/master/src/main/java/by/epam/learn/daryatarasevich/shapes/cube/comparator/IdComparator), [по имени](https://github.com/darya1500/epam_training/blob/master/src/main/java/by/epam/learn/daryatarasevich/shapes/cube/comparator/ShapeNameComparator), [по координатам Х первой точки](https://github.com/darya1500/epam_training/blob/master/src/main/java/by/epam/learn/daryatarasevich/shapes/cube/comparator/ByFirstPointXCoordinateComparator) , [по координатам Y первой
точки](https://github.com/darya1500/epam_training/blob/master/src/main/java/by/epam/learn/daryatarasevich/shapes/cube/comparator/ByFirstPointYCoordinateComparator) и т д. Использовать интерфейс [Comparator](https://github.com/darya1500/epam_training/tree/master/src/main/java/by/epam/learn/daryatarasevich/shapes/cube/comparator).
