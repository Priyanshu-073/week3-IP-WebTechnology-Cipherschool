# week3-IP-WebTechnology-Cipherschool
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta http-equiv="X-UA-Compatible" content="IE-edge" />
    <meta name="viewport" content="width-device-width, initial-scale=1.0" />
    <title>Javascript</title>
  </head>
  <body>
    <nav>
      <div class="logo">
        <h4>The Nav</h4>
      </div>
      <ul class="nav-links">
        <li>
          <a href="#">Home</a>
        </li>
        <li>
          <a href="#">About</a>
        </li>
        <li>
          <a href="#">Work</a>
        </li>
        <li>
          <a href="#">Projects</a>
        </li>
      </ul>
      <div class="burger">
        <div class="line1"></div>
        <div class="line2"></div>
        <div class="line3"></div>
      </div>
    </nav>
    <script>
          const navSlide = () => {
            const burger = document.querySelector(".burger");
            const nav = document.querySelector(".nav-links");
            const navLinks = document.querySelectorAll(".nav-links li");

            burger.addEventListener("click", () => {
              //Toggle Nav
              nav.classList.toggle("nav-active"); //this is the nav

              //Animate Links
              navLinks.forEach((link, index)) => {
                if (link.style.animation) {
                  link.style.animation = "";
                } else {
                  link.style.animation = 'navLinkFade 0.5s ease forwards ${
                    index / 7 + 0.5
                  }s';
                }
              });
              //Burger Animation
              burger.classList.toggle("toggle");
        });
      };

      navSlide();
    </script>
  </body>
</html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta http-equiv="X-UA-Compatible" content="IE-edge" />
    <meta name="viewport" content="width-device-width, initial-scale=1.0" />
    <title>Accessing elements in Javascript</title>
  </head>
  <body>
    <header class="header-content" id="header">
      <p>Welcome!</p>
    </header>
    <main>
      <img
        src="https://tse4.explicit.bing.net/th?id=OIP.NEfnNeK-4ZctK0EyWu-ASgHaFj&pid=Api&P=0"
        alt=""
        width="200px"
      />
      <p>This is the main</p>
      <p>This is the main two</p>
      <p>This is the main three</p>
      <p>This is the main four</p>
    </main>
    <footer>This is the footer</footer>

    <script>
      let type = document.querySelector("header");
      console.log(type);

      let classSelector = document.querySelector("header-content");
      console.log(classSelector);

      let idSelector = document.querySelector("#header");
      console.log(idSelector);

      let decendent = document.querySelector("header-content p");
      console.log(decendent);

      let All = document.querySelectorAll("main p");
      console.log(All);

      let bg = document
        .querySelectorAll("main p")
        .forEach((item) => (item.style.backgroundColor = "lightpink"));

      let color = document
        .querySelectorAll("main p:last-child")
        .forEach((item) => (item.style.color = "white"));

      // Older Methods
      let oldtype = document.getElementsByTagName("header");
      console.log(oldtype);

      let oldclass = document.getElementsByClassName("header-content");
      console.log(oldclass);

      let oldid = document.getElementsById("header");
      console.log(oldid);
    </script>
  </body>
</html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta http-equiv="X-UA-Compatible" content="IE-edge" />
    <meta name="viewport" content="width-device-width, initial-scale=1.0" />
    <title>modifying classes in Javascript</title>
  </head>
  <body>
    <header class="header-content container" id="header">
      <p>Welcome!</p>
    </header>
    <main>
      <img
        src="https://tse4.explicit.bing.net/th?id=OIP.NEfnNeK-4ZctK0EyWu-ASgHaFj&pid=Api&P=0"
        alt=""
        width="200px"
      />
      <p>This is the main</p>
      <p>This is the main two</p>
      <p>This is the main three</p>
      <p>This is the main four</p>
    </main>
    <footer>This is the footer</footer>

    <script>
      //   Modifying the classes in JS
      let className = document.querySelector("header").className;
      console.log(className);

      let classList = document.querySelector("header").classList;
      console.log(classList);

      let metodone = document.querySelector("main p").classList.add("newclass");

      //   let metodtwo = document.querySelector("main p").classList.remove("newclass");

      let metodthree = document
        .querySelector("main p")
        .classList.replace("newclass", "oldclass");
    </script>
  </body>
</html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta http-equiv="X-UA-Compatible" content="IE-edge" />
    <meta name="viewport" content="width-device-width, initial-scale=1.0" />
    <title>modifying attributes in Javascript</title>
  </head>
  <body>
    <header class="header-content container" id="header">
      <p>Welcome!</p>
    </header>
    <main>
      <img
        src="https://tse4.explicit.bing.net/th?id=OIP.NEfnNeK-4ZctK0EyWu-ASgHaFj&pid=Api&P=0"
        alt=""
        width="200px"
      />
      <p>This is the main</p>
      <p>This is the main two</p>
      <p>This is the main three</p>
      <p>This is the main four</p>
    </main>
    <footer>This is the footer</footer>

    <script>
      //  modifying the elements & attributes in JS

      let attribute = document.querySelector("img").attributes;
      console.log(attribute);

      let hasattribute = document.querySelector("img").hasAttribute("src");
      console.log(hasattribute);

      let getattribute = document.querySelector("img").getAttribute("src");
      console.log(getattribute);

      let setattribute = document
        .querySelector("img")
        .setAttribute(
          "src",
          "https://tse1.mm.bing.net/th?id=OIP.XFKfJK6cSKItguEeTbrjngHaEo&pid=Api&P=0"
        );

      let removeattribute = document
        .querySelector("img")
        .removeAttribute(
          "src",
          "https://tse1.mm.bing.net/th?id=OIP.XFKfJK6cSKItguEeTbrjngHaEo&pid=Api&P=0"
        );
    </script>
  </body>
</html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta http-equiv="X-UA-Compatible" content="IE-edge" />
    <meta name="viewport" content="width-device-width, initial-scale=1.0" />
    <title>modifying inline styling in Javascript</title>
  </head>
  <body>
    <header class="header-content container" id="header">
      <p>Welcome!</p>
    </header>
    <main>
      <img
        src="https://tse4.explicit.bing.net/th?id=OIP.NEfnNeK-4ZctK0EyWu-ASgHaFj&pid=Api&P=0"
        alt=""
        width="200px"
      />
      <p>This is the main</p>
      <p>This is the main two</p>
      <p>This is the main three</p>
      <p>This is the main four</p>
    </main>
    <footer style="border: 2px solid green">This is the footer</footer>

    <script>
      // modifying inlinevstyle in JS

      let footer = document.querySelector("footer").style;
      console.log(footer);

      let footerstyle = (document.querySelector(
        "footer"
      ).style.backgroundColor = "lightblue");
    </script>
  </body>
</html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta http-equiv="X-UA-Compatible" content="IE-edge" />
    <meta name="viewport" content="width-device-width, initial-scale=1.0" />
    <title>Adding DOM Elements in Javascript</title>
  </head>
  <body>
    <header class="header-content container" id="header">
      <p>Welcome!</p>
    </header>
    <main>
      <img
        src="https://tse4.explicit.bing.net/th?id=OIP.NEfnNeK-4ZctK0EyWu-ASgHaFj&pid=Api&P=0"
        alt=""
        width="200px"
      />
      <p>This is the main</p>
      <p>This is the main two</p>
      <p>This is the main three</p>
      <p>This is the main four</p>
    </main>
    <footer style="border: 2px solid green">This is the footer</footer>

    <script>
      // Adding DOM Elements in JS

      let content = "This is Bootcamp";
      let header = document.querySelector("header");
      let container = document.createElement("section");

      container.classList.add("pencil-box");
      container.setAttribute("id", "pencil");

      container.innerHTML = content;

      header.append(container);
    </script>
  </body>
</html>

<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta http-equiv="X-UA-Compatible" content="IE-edge" />
    <meta name="viewport" content=" initial-scale=1.0" />
    <title>Types of Variables</title>
  </head>
  <body>
    <h1 class="heading">Welcome to Javascript Week3</h1>
    <div>
      <div class="up-container"></div>
      <div class="bottom-container"></div>
    </div>

    <script>
      // var
      var container = 13;
      // console.log(container);

      var container = "blue";
      console.log(container);

      var x = 13,
        y = 18,
        z = 20;
      console.log(x, y, z);

      var contain;
      console.log(contain);

      // let

      // const

      // example
      var bgColor = "green";
      document.querySelector(".up-container").style.backgroundColor = bgColor;

      var bgColor = "pink";

      document.querySelector(".bottom-container").style.backgroundColor =
        bgColor;

      function heading() {
        var bgColor = "blue";
        document.querySelector(".heading").style.color = bgColor;
      }

      heading();
    </script>
  </body>
</html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta http-equiv="X-UA-Compatible" content="IE-edge" />
    <meta name="viewport" content="initial-scale=1.0" />
    <title>Datatypes in JS</title>
  </head>
  <body>
    <script>
      // string
      let string = "Text";
      console.log("string:", typeof string);

      // integer
      let integer = 13;
      console.log("number/integer:", integer);

      // float value
      let float = 3.8;
      console.log("Float value:", float);

      // boolean value
      let boolean = true;
      console.log("Boolean:", boolean);

      // null value
      let something = null;
      console.log(something);

      // undefined
      let undefinedAssign;
      console.log("Undefined:", undefined);

      // object
      const object = {
        class: "Twleveth",
        number: 50,
      };

      console.log("Object Data:", object);

      // array

      const array = ["laptop", "diary", "pens", "coffee", "code"];
      console.log("Array: ", array);
    </script>
  </body>
</html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta http-equiv="X-UA-Compatible" content="IE-edge" />
    <meta name="viewport" content="initial-scale=1.0" />
    <title>Operators in JS</title>
  </head>
  <body>
    <script>
      let a = 13;
      let b = 18;
      let c = 3.8;

      //   console.log("a:", a++);
      console.log("a:", a);

      console.log("b:", b);
      console.log("c:", c);

      let result = a * b;

      console.log("Result:", result);

      if (a !== b) {
        console.log("Yes");
      } else {
        console.log("No");
      }
    </script>
  </body>
</html>

<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta http-equiv="X-UA-Compatible" content="IE-edge" />
    <meta name="viewport" content="width-device-width, initial-scale=1.0" />
    <title>objects in JS</title>
  </head>
  <body>
    <script>
      const pencilbox = {
        name: "A Pencil Box",
        size: 30,
        color: "red",
        ziplength: {
          left: 12,
          right: 12,
          top: 24,
        },
        zipOpen: false,
        toggleZip: function (zipStatus) {
          this.zipOpen = zipStatus;
        },
      };

      console.log(pencilbox);
    </script>
  </body>
</html>
html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta http-equiv="X-UA-Compatible" content="IE-edge" />
    <meta name="viewport" content="width-device-width, initial-scale=1.0" />
    <title>Functions in JS</title>
  </head>
  <body>
    <script>
      /* Function Declarations */
      function myFunction(b, c) {
        let a = b + c;
        return a;
      }

      /* Function Expressions */
      const mySecondFuction = function (b = 13, c = 18) {
        let a = b + c;
        return a;
      };

      console.log(myFunction(13, 18));
      console.log(mySecondFunction(13, 18));

      /* Immediately Invoked Function Expression */
      (function () {
        let b = 13;
        let c = 18;
        let a = b + c;
        console.log("The sum:", a);
      })();
    </script>
  </body>
</html>
tml lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta http-equiv="X-UA-Compatible" content="IE-edge" />
    <meta name="viewport" content="width-device-width, initial-scale=1.0" />
    <title>Standard Functions in JS</title>
  </head>
  <body>
    <script>
      /* Standard functions */
      const redpencilBox = {
        name: "Red Pencil Box",
        color: "red",
        size: 30,
      };
      const bluepencilBox = {
        name: "Blue Pencil Box",
        color: "blue",
        size: 24,
      };

      const addPencilBox = function (currentPencilBox) {
        const newSection = document.createElement("section");
        newSection.innerHTML = `
        <h1>Name: ${currentPencilBox.name}</h1>
        <ul>
            <li>Color:${currentPencilBox.color} </li>
            <li>Size: ${currentPencilBox.size}</li>
        </ul>
    `;
        return newSection;
      };

      document.body.append(addPencilBox(redpencilBox));
      document.body.append(addPencilBox(bluepencilBox));
    </script>
  </body>
</html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta http-equiv="X-UA-Compatible" content="IE-edge" />
    <meta name="viewport" content="width-device-width, initial-scale=1.0" />
    <title>Arrow Functions</title>
  </head>
  <body>
    <script>
      /* Arrow Function and this keyword */
      window.size = 13;

      const yellowpencilBox = {
        name: "Yellow Pencil Box",
        color: "blue",
        size: 24,
        newSize: function (size) {
          console.log(this.size);
          this.size = size;
          console.log(this.size);
          (() => {
            console.log(this.size);
          })();
        },
      };

      console.log(yellowpencilBox.newSize(5));
    </script>
  </body>
</html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta http-equiv="X-UA-Compatible" content="IE-edge" />
    <meta name="viewport" content="width-device-width, initial-scale=1.0" />
    <title>displaying objects in browser</title>
  </head>
  <body>
    <script type="module">
      import pencilBox from "./pencilBox.js";

      const newPencilBox = new pencilBox(
        "pencil Box",
        30,
        "red",
        12,
        12,
        24,
        false,
        "2022-12-24 00:00:00"
      );

      const content = `
    <main>
        <ul>
            <li>Name: ${newPencilBox.name}</li>
            <li>Size: ${newPencilBox.size}</li>
            <li>Color: ${newPencilBox.color}</li>
            <li>Zip Length Left: ${newPencilBox.zipLength.left}</li>
            <li>Zip Length Right: ${newPencilBox.zipLength.right}</li>
            <li>Zip Length Top: ${newPencilBox.zipLength.top}</li>
            <li>Zip Status: ${newPencilBox.zipOpen}</li>
        </ul>
    </main>
`;

      document.body.innerHTML = content;

      console.log("The Pencil Box Object:", newPencilBox);
      console.log("Size:", newPencilBox.size);

      console.log("Data Purchased:", newPencilBox.datePurchased);
    </script>
  </body>
</html>

