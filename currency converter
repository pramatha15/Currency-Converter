import tkinter as tk
from tkinter import messagebox

# Function to convert currency
def currency_converter():
    try:
        amount = float(entry_amount.get())
        exchange_rate = float(entry_rate.get())
        converted_amount = amount * exchange_rate
        label_result.config(text=f"Converted Amount: {converted_amount:.2f} {selected_to_currency.get()}")
    except ValueError:
        messagebox.showerror("Input Error", "Please enter valid numerical values.")

# Setting up the main window
root = tk.Tk()
root.title("Currency Converter")

# Window Size
root.geometry("400x300")

# Title Label
label_title = tk.Label(root, text="Currency Converter", font=("Arial", 16))
label_title.pack(pady=10)

# Amount Label and Text Entry
label_amount = tk.Label(root, text="Amount:")
label_amount.pack(pady=5)
entry_amount = tk.Entry(root, width=20)
entry_amount.pack(pady=5)

# From Currency Label and Dropdown Menu
label_from_currency = tk.Label(root, text="From Currency:")
label_from_currency.pack(pady=5)
currencies = ['USD', 'EUR', 'GBP', 'INR', 'JPY', 'AUD']
selected_from_currency = tk.StringVar(root)
selected_from_currency.set(currencies[0])  # Default currency is USD
dropdown_from_currency = tk.OptionMenu(root, selected_from_currency, *currencies)
dropdown_from_currency.pack(pady=5)

# To Currency Label and Dropdown Menu
label_to_currency = tk.Label(root, text="To Currency:")
label_to_currency.pack(pady=5)
selected_to_currency = tk.StringVar(root)
selected_to_currency.set(currencies[1])  # Default currency is EUR
dropdown_to_currency = tk.OptionMenu(root, selected_to_currency, *currencies)
dropdown_to_currency.pack(pady=5)

# Exchange Rate Label and Text Entry (Optional for now)
label_rate = tk.Label(root, text="Exchange Rate (Optional):")
label_rate.pack(pady=5)
entry_rate = tk.Entry(root, width=20)
entry_rate.pack(pady=5)

# Convert Button
button_convert = tk.Button(root, text="Convert", command=currency_converter)
button_convert.pack(pady=15)

# Result Label (where the result will appear)
label_result = tk.Label(root, text="Converted Amount: 0.00", font=("Arial", 12))
label_result.pack(pady=10)

# Start the main event loop
root.mainloop()
