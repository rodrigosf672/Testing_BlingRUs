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

---
