# DOM Exercise: The Ironhack Cart

## Introduction to 'The Ironhack Cart'

Besides, we will calculate the total price of items for each product and the total price of the whole Shopping Cart.

## Exercise

### Requirements

- Use a normalize to avoid differences between browsers styles. Here you have one CDN:

https://cdnjs.cloudflare.com/ajax/libs/normalize/5.0.0/normalize.min.cs

- Use at least 3 `onclick` events
- Use at least once `getElementById`
- Use at least once `getElementsByTagName`
- Use at least once `getElementsByClassName`

### Iteration 1: Creating one product

We will start by creating the HTML for one of your products. It will look like this:

![](https://i.imgur.com/gDZ1Lj0.png)

Every product will have:
- A div with a span showing the product name
- A div with a span showing the cost of one unit
- A div with one label and one input for the client to indicate the desired quantity of items
- A div with a span showing the total price of those items. This is the result of calculating the number of items multiplied by the price of one product. The total price will be 0 by default
- A div with a delete button to drop the product from the list

#### Calculating the total price

Once you have the HTML and CSS prepared, use JavaScript to retrieve the data you need to calculate the total price and change the value in the DOM.

- Create a click event for the `Calculate Prices` button
- This event will execute a function that:
	* Retrieves the unit price of the product
	* Retrieves the quantity of items desired
	* Calculates the total price based on this data
	* Updates the total price in the DOM

### Iteration 2: Creating a second product

Create a second product.

![](https://i.imgur.com/Fe48iGO.png)

When you click on the `Calculate Prices` button every price should be updated at the same time.

### Iteration 3: Calculating the Ironhack Cart total price

We will sum all the prices of each product to calculate the total price of the shopping cart. Then, show the result in the DOM.

![](https://i.imgur.com/u607NQ0.png)

Create a new `div` below the `Calculate Prices` button. This `div` will have an `h2` element showing:

`<h2>Total Price: <span>$0</span></h2>`

Also, we need to create a function that will:

- Select the totals for each product
- Sum all the elements selected in the previous step to calculate the Ironhack cart's total price
- Show the Ironhack cart's total price in the DOM

### Iteration 4: Deleting a product

We will create a click event binded to the Delete buttons to delete a product from the list. To do this, we need to:

- Select all the `Delete` buttons
- Assign a click event for them that will:
	- Select the div that contains the HTML element of the product we want to delete
	- Select the div that contains the product list
	- Use the function `removeChild` we saw in [DOM Manipulators](https://hackmd.io/MwBgRgHAjATArMAtANjsgxogLAU3QQ0QmQHZlEdgox8BOE9EsAMzCA==)

:::success
:bulb: Remember it is possible to track which button was clicked by the `e.currentTarget` function, and select the parent node of an HTML element with `parentNode`.
:::

### Iteration 5: Creating new products

We will create dynamically new products for the shop. The form will look like this:

![](https://i.imgur.com/FGVUuHt.png)

We have two inputs that represents the name and the unit price of the new product. At the end, we will add a button to create that product.

- Create two inputs to retrieve the data of your new product.
- Create a button. This button will have assigned a click event that will:
	- Get the data from the inputs.
	- Create a new product row with the data we stored.

:::warning
:warning: Be sure the new product you added has the same behavior than the prefixed products.
- You can calculate the product total price
- You can sum the product total price to the Shopping Cart total price
- You can delete the product
:::
