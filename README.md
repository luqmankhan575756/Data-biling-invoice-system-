<!-- Billing & Invoice System in Python -->
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Billing & Invoice System in Python</title>
</head>
<body>
  <h1>🧾 Billing & Invoice System in Python</h1>

  <p>This project is a simple console-based Billing System written in Python.  
  It allows users to input multiple items, their quantities, and prices, and then automatically calculates the subtotal, tax, and total bill amount.</p>

  <h2>💡 Features</h2>
  <ul>
    <li>Input any number of items</li>
    <li>Automatically calculates subtotal, 5% tax, and total bill</li>
    <li>Displays a clean, formatted invoice</li>
  </ul>

  <h2>🧰 Requirements</h2>
  <ul>
    <li>Python 3.7 or above</li>
    <li>No external libraries needed (uses built-in functions only)</li>
  </ul>

  <h2>🚀 How to Run</h2>
  <ol>
    <li>Save the code below as <code>billing_system.py</code></li>
    <li>Open a terminal or command prompt</li>
    <li>Run: <code>python billing_system.py</code></li>
  </ol>

  <h2>📜 Python Code</h2>
  <pre><code>
print("----- Welcome to Billing System -----")

items = []  # To store item names
prices = [] # To store item prices
qtys = []   # To store quantities

tax_rate = 0.05  # 5% tax

while True:
    item = input("Enter item name (or type 'done' to finish): ")
    if item.lower() == "done":
        break

    qty = int(input("Enter quantity: "))
    price = float(input("Enter price per item: "))

    items.append(item)
    qtys.append(qty)
    prices.append(price)

# Display Invoice
print("\n=========== INVOICE ===========")
total = 0

for i in range(len(items)):
    cost = prices[i] * qtys[i]
    total += cost
    print(f"{items[i]}  x{qtys[i]}  = Rs {cost}")

tax = total * tax_rate
grand_total = total + tax

print("--------------------------------")
print(f"Subtotal: Rs {total}")
print(f"Tax (5%): Rs {tax:.2f}")
print(f"Total Bill: Rs {grand_total:.2f}")
print("======= Thank You! Visit Again =======")
  </code></pre>

  <h2>🧾 Sample Output</h2>
  <pre>
----- Welcome to Billing System -----
Enter item name (or type 'done' to finish): Apple
Enter quantity: 3
Enter price per item: 100
Enter item name (or type 'done' to finish): Banana
Enter quantity: 5
Enter price per item: 50
Enter item name (or type 'done' to finish): done

=========== INVOICE ===========
Apple  x3  = Rs 300
Banana  x5  = Rs 250
--------------------------------
Subtotal: Rs 550
Tax (5%): Rs 27.50
Total Bill: Rs 577.50
======= Thank You! Visit Again =======
  </pre>

  <h2>📁 Project Summary</h2>
  <ul>
    <li><strong>
