# Bling R Us Pricing and Engraving Calculator

This Python script calculates the total cost of an order for Bling R Us, based on a set of products with predefined base prices, engraving specifications, discounts, VAT, and shipping rules. This draft version was created as a testing solution for the Bling R Us website’s pricing system, with the potential to be further developed for automated testing using Selenium WebDriver.

## Challenge Context

Challenge based on the [Bling R Us website](https://blingrus.azurewebsites.net), where pricing and engraving rules determine the final cost of customized products. This script was written to test the pricing logic accurately, adhering to the provided rules for each product.

---

### Step 1: Gathering Product Order Information

The `get_product_order` function collects information on the products the customer wants, including quantities and engraving text (if applicable). Engraving messages can have multiple lines, indicated by the use of `/` to separate lines. For each product, the following inputs are requested:
- **Product Name**
- **Quantity**
- **Engraving Text** (optional)

### Step 2: Engraving Cost Calculation

The `engraving_cost` function calculates the cost of engraving based on the number of characters and lines. Specific rules include:
- A base cost of 50 SEK for engraving with more than 10 characters.
- An additional 50 SEK for every 10 characters over 30.
- Additional charges per line beyond the first, except for "The Twin" and "The Twin Towers."

### Step 3: Order Cost Calculation

The `order_cost` function calculates the total cost of the order, which includes:
1. **Base Price Calculation**: The base price for each product is multiplied by the quantity ordered.
2. **Discounts**: 
   - 10% discount on orders with more than 4 items.
   - Every 5th product is free.
3. **VAT**: A 25% VAT is applied to the subtotal.
4. **Shipping**: Free shipping for orders above 250 SEK; otherwise, shipping is 36 SEK per product.

The function outputs the **total cost of the order** in SEK, inclusive of all applicable discounts, VAT, and shipping fees.

---

## How to Use

1. Run the script in a Python environment.
2. Input the requested product names, quantities, and engraving messages when prompted.
3. The total cost will be displayed upon completion.

--- 

## Future Improvements

This script can serve as a base for a more automated testing solution. By integrating it with Selenium WebDriver, it would be possible to:
- Automatically input data into the Bling R Us website.
- Test shopping cart functionalities.
- Validate pricing and engraving calculations directly on the website.
