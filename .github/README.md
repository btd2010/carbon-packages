# carbon-packages
I write many basic packages that make writing Carbon a little bit easier. All of my one-file packages and their usage are shared here.

## Table Of Contents
- [Shapes](#shapes)
    - [Classes](#shapes-classes)
    - [Examples](#shapes-examples)

## Shapes
```cpp
import Shapes
```
Provides many different functions and classes to deal with shapes. Other than basic calculators, this would only be super useful in drawing UI to the screen.

### Shapes: Classes
- ``Circle``
    - ``Radius``: Radius of the circle.
    - **Const** ``Diameter``: Diameter of the circle.
    - **Const** ``Pi``: 3.141592653...

    - **Function** ``Area()``: Returns area of the circle.
    - **Function** ``Circumference()``: Returns circumference of the circle.
- ``Rectangle``
    - ``Width``: Width of the rectangle.
    - ``Height``: Height of the rectangle.

    - **Function** ``Area()``: Returns area of the rectangle.
- ``Square``
    - **NOTE!** Square is a duplicate of ``Rectangle``. It provides the same functions and variables.
- ``Triangle``
    - ``Width``: Width of the triangle.
    - ``Height``: Height of the triangle.
    - **Function** ``Area()``: Returns area of the triangle.
- ``Hexagon``:
    - ``Side``: Define the length of one side of the hexagon.
    - **Function** ``Area()``: Returns area of the hexagon.
### Shapes: Examples
#### Do basic math with a circle
```cpp
import Shapes;

fn Main() -> i32 {
    var Circle: Shapes.Circle = {
        Radius = 10;
    }

    Print(Circle.Area()); // 314 (roughly)
    Print(Circle.Pi()); // 3.141592653...

    return 0;
}
```
#### Use a square to create graphics
> Note: There is no real general graphics library yet, this is only an example of a use case.
```cpp
fn GenerateGraphic(nwidth: i32, nheight: i32) {
    var NewRectangle: Shapes.Rectangle { Width = nwidth, Height = nheight }
    return NewRectangle
}
```