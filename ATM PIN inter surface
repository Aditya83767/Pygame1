# ATM PIN Setup Interface
# Import necessary libraries
from tkinter import *
 
# Create Window
root = Tk()
root.title("ATM PIN Setup Interface")
root.geometry("400x500")
 
# Create a frame to organize account details
details_frame = Frame(
    master=root,
    height=150,
    width=360,
    bg="#d0efff"
)
 
# Add labels
name_label = Label(
    details_frame,
    text="Account Name",
    bg="#3895D3",
    fg="white",
    width=14
)
 
pin_label = Label(
    details_frame,
    text="Create PIN",
    bg="#3895D3",
    fg="white",
    width=14
)
 
# Create entry widgets
name_entry = Entry(details_frame)
 
# show="*" hides the entered PIN
pin_entry = Entry(details_frame, show="*")
 
 
# Function to confirm the PIN setup
def confirm_pin():
    # Read input from the Entry widgets
    account_name = name_entry.get()
    pin = pin_entry.get()
 
    # Clear the previous message
    message_box.delete(1.0, END)
 
    # Check whether all details are entered
    if account_name == "" or pin == "":
        message_box.insert(
            END,
            "Please enter the account name and PIN."
        )
    else:
        message = (
            "Hello " + account_name +
            "\nYour ATM PIN has been set successfully."
        )
        message_box.insert(END, message)
 
 
# Create a frame for the number-pad cells
keypad_frame = Frame(
    master=root,
    relief=SUNKEN,
    borderwidth=2
)
 
# Number-pad values
numbers = [
    [1, 2, 3],
    [4, 5, 6],
    [7, 8, 9],
    ["Clear", 0, "Enter"]
]
 
# Build the number-pad grid
for i in range(4):
    keypad_frame.rowconfigure(i, weight=1, minsize=40)
 
    for j in range(3):
        keypad_frame.columnconfigure(j, weight=1, minsize=70)
 
        # Create a bordered cell
        cell = Frame(
            master=keypad_frame,
            relief=RAISED,
            borderwidth=1
        )
 
        cell.grid(
            row=i,
            column=j,
            sticky="nsew"
        )
 
        # Display the number inside the cell
        number_label = Label(
            master=cell,
            text=numbers[i][j],
            bg="#d0efff"
        )
 
        number_label.pack(
            padx=8,
            pady=8
        )
 
 
# Create confirmation button
confirm_button = Button(
    root,
    text="Set ATM PIN",
    command=confirm_pin,
    bg="red",
    fg="white"
)
 
# Create text widget to display the result
message_box = Text(
    root,
    height=5,
    width=42,
    bg="#BEBEBE",
    fg="black"
)
 
# Position widgets exactly using place()
details_frame.place(x=20, y=10)
 
name_label.place(x=15, y=25)
name_entry.place(x=155, y=25)
 
pin_label.place(x=15, y=85)
pin_entry.place(x=155, y=85)
 
keypad_frame.place(x=85, y=180)
 
confirm_button.place(x=145, y=370)
 
message_box.place(x=25, y=410)
 
# Start the GUI event loop
root.mainloop()
