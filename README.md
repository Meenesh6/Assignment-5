abstract class Shape {
    abstract double area();
}

// Circle class
class Circle extends Shape {
    private double radius;

    Circle(double radius) {
        this.radius = radius;
    }

    @Override
    double area() {
        return Math.PI * radius * radius;
    }
}

// Rectangle class
class Rectangle extends Shape {
    private double length, width;

    Rectangle(double length, double width) {
        this.length = length;
        this.width = width;
    }

    @Override
    double area() {
        return length * width;
    }
}

// Triangle class
class Triangle extends Shape {
    private double base, height;

    Triangle(double base, double height) {
        this.base = base;
        this.height = height;
    }

    @Override
    double area() {
        return 0.5 * base * height;
    }
}

// Main class to test
public class Main {
    public static void main(String[] args) {
        Shape[] shapes = {
            new Circle(5),
            new Rectangle(4, 6),
            new Triangle(3, 7)
        };

        for (Shape shape : shapes) {
            System.out.printf("%s area: %.2f%n",
                shape.getClass().getSimpleName(),
                shape.area());
        }
    }
} 
Output 
Circle area: 78.54
Rectangle area: 24.00
Triangle area: 10.50
# Assignment-5
