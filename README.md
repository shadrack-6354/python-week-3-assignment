# python-week-3-assignment
# Define the function to calculate the discount
def calculate_discount(price, discount_percent):
    # Check if the discount is 20% or higher
    if discount_percent >= 20:
        # Apply the discount
        final_price = price - (price * (discount_percent / 100))
        return final_price
    else:
        # No discount applied, return the original price
        return price

# Prompt the user to enter the original price and discount percentage
price = float(input("Enter the original price of the item: "))
discount_percent = float(input("Enter the discount percentage: "))

# Call the function to calculate the final price
final_price = calculate_discount(price, discount_percent)

# Print the final price after applying the discount (if applicable)
if final_price != price:
    print(f"The final price after applying the discount is: ${final_price:.2f}")
else:
    print(f"No discount applied. The original price is: ${price:.2f}")
