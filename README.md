// Base class
class Shape {
  constructor(color) {
    this.color = color;
  }

  getColor() {
    console.log(Color: ${this.color});
  }

  area() {
    console.log('Calculating area...');
  }
}

// Derived class
class Circle extends Shape {
  constructor(color, radius) {
    super(color);
    this.radius = radius;
  }

  area() {
    const circleArea = Math.PI * this.radius * this.radius;
    console.log(Circle Area: ${circleArea.toFixed(2)});
  }
}

// Derived class
class Rectangle extends Shape {
  constructor(color, width, height) {
    super(color);
    this.width = width;
    this.height = height;
  }

  area() {
    const rectangleArea = this.width * this.height;
    console.log(Rectangle Area: ${rectangleArea});
  }
}

// Create instances of the derived classes
const redCircle = new Circle('red', 5);
const blueRectangle = new Rectangle('blue', 4, 6);

// Use the inherited methods
redCircle.getColor(); // Output: Color: red
redCircle.area();     // Output: Circle Area: 78.54

blueRectangle.getColor(); // Output: Color: blue
blueRectangle.area();     // Output: Rectangle Area: 24
