from tkinter import *
from tkinter import messagebox
from random import randint
import sys

root = Tk()
root.title("Menu")
root.iconbitmap("C:/python/menuICO.ico")
root.configure(bg="#141414")

#Starter balance and price
balance = randint(5, 100)

#Showing menu and balance to customer
menu = Label(root, text="Menu:", bg="orange", borderwidth=7).grid(row=0, column=0, columnspan=3, sticky=W)
showbalance = Label(root, text="Your balance: " + str(balance) +"$", bg="orange", borderwidth=7).grid(row=0, column=2, sticky=E)

#Showing ordered foods and cost to customer
def update_text():
	global bill
	foods = ""
	price = 0
	if chicken.get():
		foods += "Chicken with sauce | "
		price += 15
	if pizza1.get():
		foods += "Pepperoni Pizza | "
		price += 20
	if pizza2.get():
		foods += "Margarita Pizza | "
		price += 20
	if steak.get():
		foods += "Steak | "
		price += 30
	if cheeseburger.get():
		foods += "Cheeseburger | "
		price += 9
	if soup.get():
		foods += "Soup | "
		price += 4
	if cake.get():
		foods += "Cake | "
		price += 12
	if cookies.get():
		foods += "Cookies | "
		price += 4
	if cheesecake.get():
		foods += "Cheesecake | "
		price += 10
	if icecream.get():
		foods += "Ice cream | "
		price += 5
	if pudding1.get():
		foods += "Pudding (Chocolate) | "
		price += 6
	if pudding2.get():
		foods += "Pudding (Banana) | "
		price += 6
	if water.get():
		foods += "Water | "
		price += 2
	if coke.get():
		foods += "Coke | "
		price += 3
	if tea.get():
		foods += "Tea | "
		price += 3.5
	if coffee.get():
		foods += "Coffee | "
		price += 4
	if milkshake1.get():
		foods += "Milkshake (Orange) | "
		price += 4.5
	if milkshake2.get():
		foods += "Milkshake (Banana) | "
		price += 4.5
	if edrink.get():
		foods += "Energy Drink | "
		price += 5
	foods += "\n\nTotal cost: " + str(price)
	bill.delete(0.0, END)
	bill.insert(0.0, foods)
	return price

#Checking if money is enough or not
def check_money(price):
	global balance
	global bill
	if price > balance:
		messagebox.showerror("Check your wallet", "Not enough money!")
	else:
		balance -= price
		showbalance = Label(root, text="   Your balance: " + str(balance) +"$", bg="orange", borderwidth=7).grid(row=0, column=2, sticky=E)
		ask = messagebox.askyesno("", "Here is your receipt, Sir! 🗂\n\n"\
			"Anything else?")
		if ask == 0:
			sys.exit()
		bill.delete(0.0, END)


#Putting foods in a frame for better look
frame1 = LabelFrame(root, text="Hot Dishes", bg="#141414", fg="orange", padx=5, pady=5)
frame2 = LabelFrame(root, text="Desserts", bg="#141414", fg="orange", padx=5, pady=5)
frame3 = LabelFrame(root, text="Beverages", bg="#141414", fg="orange", padx=5, pady=5)
frame1.grid(row=3, column=0, padx=10,pady=10)
frame2.grid(row=3, column=1, padx=10,pady=10)
frame3.grid(row=3, column=2, padx=10,pady=10)

#Hotdish checkbuttons
chicken = BooleanVar()
pizza1 = BooleanVar()
pizza2 = BooleanVar()
steak = BooleanVar()
cheeseburger = BooleanVar()
soup = BooleanVar()
Checkbutton(frame1, text="🍗 Chicken with sauce   -   15$", variable=chicken, bg="#141414", fg="orange", command=update_text).grid(row=4, column=0, sticky=W)
Checkbutton(frame1, text="🍕 Pepperoni Pizza   -   20$", variable=pizza1, bg="#141414", fg="orange", command=update_text).grid(row=5, column=0, sticky=W)
Checkbutton(frame1, text="🍕 Margarita Pizza   -   20$", variable=pizza2, bg="#141414", fg="orange", command=update_text).grid(row=6, column=0, sticky=W)
Checkbutton(frame1, text="🥩 Steak   -   30$", variable=steak, bg="#141414", fg="orange", command=update_text).grid(row=7, column=0, sticky=W)
Checkbutton(frame1, text="🍔 Cheeseburger   -   9$", variable=cheeseburger, bg="#141414", fg="orange", command=update_text).grid(row=8, column=0, sticky=W)
Checkbutton(frame1, text="🍲 Soup   -   4$", variable=soup, bg="#141414", fg="orange", command=update_text).grid(row=9, column=0, sticky=W)

cake = BooleanVar()
cookies = BooleanVar()
cheesecake = BooleanVar()
icecream = BooleanVar()
pudding1 = BooleanVar()
pudding2 = BooleanVar()

#Dessert checkbuttons
Checkbutton(frame2, text="🎂 Cake   -   12$", variable=cake, bg="#141414", fg="orange", command=update_text).grid(row=4, column=2, sticky=W)
Checkbutton(frame2, text="🍪 Cookies (3)   -   4$", variable=cookies, bg="#141414", fg="orange", command=update_text).grid(row=5, column=2, sticky=W)
Checkbutton(frame2, text="🍰 Cheesecake   -   10$", variable=cheesecake, bg="#141414", fg="orange", command=update_text).grid(row=6, column=2, sticky=W)
Checkbutton(frame2, text="🍨 Ice cream (Vanilla)   -   5$", variable=icecream, bg="#141414", fg="orange", command=update_text).grid(row=7, column=2, sticky=W)
Checkbutton(frame2, text="🍮 Pudding (Chocolate)   -   6$", variable=pudding1, bg="#141414", fg="orange", command=update_text).grid(row=8, column=2, sticky=W)
Checkbutton(frame2, text="🍮 Pudding (Banana)   -   6$", variable=pudding2, bg="#141414", fg="orange", command=update_text).grid(row=9, column=2, sticky=W)

water = BooleanVar()
coke = BooleanVar()
tea = BooleanVar()
coffee = BooleanVar()
milkshake1 = BooleanVar()
milkshake2 = BooleanVar()
edrink = BooleanVar()
#Beverage checkbuttons
Checkbutton(frame3, text="🍶 Water   -   2$", variable=water, bg="#141414", fg="orange", command=update_text).grid(row=4, column=3, sticky=W)
Checkbutton(frame3, text="🥤 Coke   -   3$", variable=coke, bg="#141414", fg="orange", command=update_text).grid(row=5, column=3, sticky=W)
Checkbutton(frame3, text="🍵 Tea   -   3.5$", variable=tea, bg="#141414", fg="orange", command=update_text).grid(row=6, column=3, sticky=W)
Checkbutton(frame3, text="☕ Coffee   -   4$", variable=coffee, bg="#141414", fg="orange", command=update_text).grid(row=7, column=3, sticky=W)
Checkbutton(frame3, text="🍼 Milkshake (Orange)   -   4.5$", variable=milkshake1, bg="#141414", fg="orange", command=update_text).grid(row=8, column=3, sticky=W)
Checkbutton(frame3, text="🍼 Milkshake (Banana)   -   4.5$", variable=milkshake2, bg="#141414", fg="orange", command=update_text).grid(row=9, column=3, sticky=W)
Checkbutton(frame3, text="⚡🥃 Energy Drink   -   5$", variable=edrink, bg="#141414", fg="orange", command=update_text).grid(row=10, column=3, sticky=W)

#Order and bill text & pay button
order = Label(root, text="Your order:", bg="orange", borderwidth=7)
pay = Button(root, text="Pay", bg="orange", borderwidth=7, command = lambda: check_money(update_text()))
bill = Text(root, width=60, height=10, borderwidth=5, bg="#FFDEAD", wrap = WORD)

order.grid(row=11, sticky=W)
bill.grid(row=12, columnspan=6, sticky=W)
pay.grid(row=12, column=2)


mainloop()
