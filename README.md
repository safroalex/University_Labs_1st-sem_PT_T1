# University_Labs_1st-sem_T1
This repository was created for the first lab in Programming Technologies - a university subject.

Task:

Все числовые данные в этой работе должны быть представлены значениями с плавающей запятой.
Использование контейнеров стандартной библиотеки в настоящей работе недопустимо (за исключением
std::string для обработки ввода)
1. Создать файл base-types.hpp, содержащий определения следующих структур:
• point_t, представляющую собой точку на плоскости, координаты должны храниться в полях
x и y.
• rectangle_t, описывающую прямоугольник шириной width и высотой height с центром в точке
pos.
2. Создать файл shape.hpp, содержащий определение абстрактного класса Shape. Этот класс должен
предоставлять следующие методы:
getArea вычисление площади
getFrameRect получение ограничивающего прямоугольника для фигуры (см. типы из предыдущего пункта), стороны ограничивающего прямоугольника всегда параллельны осям
move перемещение центра фигуры, 2 варианта: в конкретную точку и в виде смещений по осям
абсцисс и ординат
scale изотропное масштабирование фигуры относительно её центра с указанным коэффициентом
3. Реализовать класс Rectangle в файлах rectangle.hpp и rectangle.cpp, соответственно.
4. Дополнительно реализовать ещё 2 (две) геометрические фигуры, указанные преподавателем.
5. Продемонстрировать правильную работу классов программой, демонстрирующей полиморфное применение классов.
• Программа должна быть реализована в виде 1-го исполняемого файла, не обрабатывающего
параметры командной строки.
• Программа должна обрабатывать поток стандартного ввода, содержащий описание геометрических фигур. Каждая строка гарантировано содержит описание не более одной фигуры. Элементы в описании разделены ровно одним пробелом и гарантировано являются вещественными
числами (за исключением названия фигур) Описание завершается командой масштабирования
фигур. Пример описания:

CIRCLE 1.15 2.5 10.1

RECTANGLE -5.9 -3.4 3.0 4.0

SQUARE -1.55 -1.55 10.5

TRIANGLE 1.3 2.2 3.2 5.0 10.0 -5.5

POLYGON 1.3 2.2 3.2 5.0 10.0 -5.5

SCALE -15.0 -7.5 1.5

• Каждая фигура описывается своим набором параметров. Отсутствие самопересечений, выпуклость фигур и корректное количество, и только количество, параметров гарантируется, если не
сказано иного:

– Прямоугольник описывается парой координат своих углов: левым нижним и правым верхним. Считайте, что стороны прямоугольника параллельны осям координат. Центром фигуры считайте точку пересечения диагоналей

RECTANGLE 1.0 1.0 3.0 4.0

RECTANGLE 0.0 0.0 -2.0 -10.0

– Эллипс описывается координатами центра и двумя значениями радиусов: по вертикальной
оси и по горизонатльной оси. Считайте, что оси эллипса параллельны осям координатам.
Центром эллипса считайте точку пересечения осей эллипса

ELLIPSE 0.0 0.0 10.0 20.0

– Четырёхугольник с самопересечениями задаётся координатами двух своих пересекающихся
сторон. Центром фигуры считайте точку пересечения этих сторон. Кроме того, считайте,
что первая и последняя вершины в описании формируют сторону фигуры

COMPLEXQUAD 0.0 0.0 10.0 10.0 2.0 0.0 3.0 0.0
