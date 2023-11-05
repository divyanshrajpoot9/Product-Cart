# Product-Cart
### Hosted Link: 
### Java Script DOM Manipulation:
The Document Object Model (DOM) is a programming interface for web documents. It provides a structured representation of a web page, allowing you to access and manipulate its elements and content using JavaScript. Here are some basic DOM properties and methods.
document: The document object represents the entire HTML document and serves as the entry point to the DOM. It provides properties and methods to access and modify the document's structure, content, and style.

### Element Selection and Traversal:

  ### getElementById(id): Retrieves an element by its unique id attribute.
  #### getElementsByClassName(className): Returns a collection of elements with a specific class name.
  ####  getElementsByTagName(tagName): Returns a collection of elements with a specific tag name.
  ####  querySelector(selector): Returns the first element that matches the CSS selector.
  ####  querySelectorAll(selector): Returns a list of all elements that match the CSS selector.

  This code is a JavaScript implementation of a simple shopping cart application that allows users to view a list of products, add them to a shopping cart, remove them from the cart, and see the total price of the items in the cart. Let's break down the code step by step:

1. **Product Data**: The code starts by defining an array called `Products`, which contains information about different products. Each product is represented as an object with properties like `id`, `name`, and `price`.

2. **DOM Elements**: The code then defines several variables to capture references to HTML elements in the DOM (Document Object Model). These elements include:

   - `productListView`: Represents a list where the products will be displayed.
   - `shoppingCartListView`: Represents a list where the items in the shopping cart will be displayed.
   - `cartStatus`: An element that is displayed when the shopping cart is empty.
   - `totalPriceDisplay`: An element to display the total price of the items in the cart.
   - `cart`: An array to store the items in the shopping cart.

3. **`renderProductList` Function**: This function is responsible for rendering the list of products. It clears the existing content of `productListView` and then iterates over the `Products` array, creating an HTML list item for each product. It displays the product name, price, and provides buttons to add or remove items from the cart.

4. **`renderShoppingCart` Function**: This function renders the shopping cart. It clears the existing content of `shoppingCartListView` and updates the quantity display for each product in the cart. It calculates and displays the total price of items in the cart.

5. **`addToCart` Function**: When a user clicks the "+" button next to a product, this function is called. It takes the `productId` as a parameter, finds the corresponding product in the `Products` array, and adds it to the shopping cart. If the product is already in the cart, it increments the quantity; otherwise, it adds a new entry to the `cart` array. After modifying the cart, it calls `renderShoppingCart` to update the UI.

6. **`removeFromCart` Function**: When a user clicks the "-" button next to a product in the cart, this function is called. It takes the `productId` as a parameter, finds the corresponding product in the `cart` array, and reduces the quantity. If the quantity becomes zero, it removes the product from the cart. The UI is updated using `renderShoppingCart`.

7. **Initialization**: The code listens for the "DOMContentLoaded" event to ensure that the DOM is fully loaded before running. It calls `renderProductList` and `renderShoppingCart` to display the initial product list and an empty shopping cart.

The code follows a simple approach to manage a shopping cart and update the UI as users interact with it. It uses event listeners on the HTML elements' buttons to trigger actions like adding and removing items from the cart. The cart's state is stored in the `cart` array, and the UI is updated based on this state.
