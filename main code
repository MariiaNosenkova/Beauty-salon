import tkinter
from tkinter import ttk
from tkinter import messagebox
# from tkcalendar import Calendar
import calendar
import csv
import matplotlib.pyplot as plt
class Appointment():
    def __init__(self):
        self.phone = ''
        self.name = ''
        self.date = ''
        self.reminder = False
        self.haircut_type = ''
        self.haircut_price = 0
        self.manicure_type = ''
        self.manicure_price = 0
        self.facial_type = ''
        self.facial_price = 0
        self.massage_type = ''
        self.massage_price = 0
        self.discount = 0
        self.total_price = 0


    def set_haircut(self, type, price):
        self.haircut_type = type
        self.haircut_price = price

    def set_manicure(self, type, price):
        self.manicure_type = type
        self.manicure_price = price

    def set_facial(self, type, price):
        self.facial_type = type
        self.facial_price = price

    def set_massage(self, type, price):
        self.massage_type = type
        self.massage_price = price

    def calculate_total(self):
        total = (self.haircut_price +
                 self.manicure_price +
                 self.facial_price +
                 self.massage_price)
        discounted_total = total * (1 - 5)
        self.total_price = discounted_total

dataFileName = 'Appointments.csv'

def save_appointment(appointment):
    with open(dataFileName, 'a') as dataFile:
        writer_csv = csv.writer(dataFile)
        writer_csv.writerow([
            appointment.phone,
            appointment.name,
            appointment.date,
            appointment.reminder,
            appointment.haircut_type,
            appointment.haircut_price,
            appointment.manicure_type,
            appointment.manicure_price,
            appointment.facial_type,
            appointment.facial_price,
            appointment.massage_type,
            appointment.massage_price,
            appointment.discount,
            appointment.total_price
        ])

def get_appointment():
    appointment = Appointment()
    appointment.phone = userTelephoneTxt.get()
    appointment.name = userNameTxt.get()
    appointment.date = userDateAppointmentTxt.get()
    appointment.reminder = userRemindercombo.get()
    appointment.haircut_type = serviceHairTypeCombo.get()
    appointment.haircut_price = serviceHairPriceCombo.get()
    appointment.manicure_type = serviceManicureTypeCombo.get()
    appointment.manicure_price = serviceManicurePriceCombo.get()
    appointment.facial_type = serviceFacialTypeCombo.get()
    appointment.facial_price = serviceFacialPriceCombo.get()
    appointment.massage_type = serviceMassageTypeCombo.get()
    appointment.massage_price = serviceMassagePriceCombo.get()
    appointment.discount = userDiscountCombo.get()
    return appointment

def save_button():
    appointment = get_appointment()
    save_appointment(appointment)
    if userNameTxt == '' or userTelephoneTxt == '' or userDateAppointmentTxt == '':
        tkinter.messagebox.showwarning(title='Error', message='Please, fill customer information')
    else:
        print('Appointment is saved')

def check_button():
    pass

def regular():
    pass

window = tkinter.Tk()
window.title('BEAUTY SALON')

frame = tkinter.Frame(window)
frame.pack()

openFrameworks = tkinter.LabelFrame(frame, highlightcolor='green', text='Customer details')
openFrameworks.grid(row=0, column=0)

userNameLabel = tkinter.Label(openFrameworks, text='Customer')
userNameLabel.grid(row=1, column=0)

userNameTxt = tkinter.Entry(openFrameworks)
userNameTxt.grid(row= 1, column= 1)

userTelephoneLabel = tkinter.Label(openFrameworks, text='Telephone No: ')
userTelephoneLabel.grid(row=1, column=2)

userTelephoneTxt = tkinter.Entry(openFrameworks)
userTelephoneTxt.grid(row= 1, column= 3)

userDateAppointmentLabel = tkinter.Label(openFrameworks, text='Date of appointment: ')
userDateAppointmentLabel.grid(row=2, column=0)

userDateAppointmentTxt = tkinter.Spinbox(openFrameworks)
userDateAppointmentTxt.grid(row= 2, column= 1)

userRemiderLabel = tkinter.Label(openFrameworks, text = 'Remind: ')
userRemiderLabel.grid(row = 2, column = 2)

userRemindercombo= ttk.Combobox(openFrameworks, values = ['Yes', 'No'])
userRemindercombo.grid(row = 2, column = 3)


openSecondFrameworks = tkinter.LabelFrame(frame, fg ='red', text='Services: ')
openSecondFrameworks.grid(row=1, column=0)

serviceHaircutLabel = tkinter.Label(openSecondFrameworks, text = 'Haircut')
serviceHaircutLabel.grid(row = 0, column = 0)

serviceHaircutCombo = ttk.Checkbutton(openSecondFrameworks, command= regular)
serviceHaircutCombo.grid(row = 0, column = 1)

serviceHairTypeLabel = tkinter.Label(openSecondFrameworks, text = 'Type: ')
serviceHairTypeLabel.grid(row = 1, column = 0)

serviceHairTypeCombo= ttk.Combobox(openSecondFrameworks, values = ['Long', 'Middle', 'Short'])
serviceHairTypeCombo.grid(row = 1, column = 1)

serviceHairPriceLabel = tkinter.Label(openSecondFrameworks, text = 'Price: ')
serviceHairPriceLabel.grid(row = 1, column = 2)

serviceHairPriceCombo= ttk.Combobox(openSecondFrameworks, values = [45.00, 35.00, 30.00])
serviceHairTypeCombo.grid(row = 1, column = 3)

serviceManicureLabel = tkinter.Label(openSecondFrameworks, text = 'Manicure')
serviceManicureLabel.grid(row = 2, column = 0)

serviceManicureCombo = ttk.Checkbutton(openSecondFrameworks, command = regular)
serviceManicureCombo.grid(row = 2, column = 1)

serviceManicureTypeLabel = tkinter.Label(openSecondFrameworks, text = 'Type: ')
serviceManicureTypeLabel.grid(row = 3, column = 0)

serviceManicureTypeCombo= ttk.Combobox(openSecondFrameworks, values = ['French', 'Classic', 'Gel', 'Basic', 'Gel/Decor'])
serviceManicureTypeCombo.grid(row = 3, column = 1)

serviceManicurePriceLabel = tkinter.Label(openSecondFrameworks, text = 'Price: ')
serviceManicurePriceLabel.grid(row = 3, column = 2)

serviceManicurePriceCombo= ttk.Combobox(openSecondFrameworks, values = [45.00, 30.00, 55.00, 25, 85])
serviceManicurePriceCombo.grid(row = 3, column = 3)

serviceFacialLabel = tkinter.Label(openSecondFrameworks, text = 'Facial')
serviceFacialLabel.grid(row = 4, column = 0)

serviceFacialCombo = ttk.Checkbutton(openSecondFrameworks, command = regular)
serviceFacialCombo.grid(row = 4, column = 1)

serviceFacialTypeLabel = tkinter.Label(openSecondFrameworks, text = 'Type: ')
serviceFacialTypeLabel.grid(row = 5, column = 0)

serviceFacialTypeCombo= ttk.Combobox(openSecondFrameworks, values = ['Oil skin', 'Anti-age', 'R-lifting', 'Spa day', 'Peeling'])
serviceFacialTypeCombo.grid(row = 5, column = 1)

serviceFacialPriceLabel = tkinter.Label(openSecondFrameworks, text = 'Price: ')
serviceFacialPriceLabel.grid(row = 5, column = 2)

serviceFacialPriceCombo= ttk.Combobox(openSecondFrameworks, values = [125.00, 150.00, 148.00, 225.00, 85.00])
serviceFacialPriceCombo.grid(row = 5, column = 3)

serviceMassageLabel = tkinter.Label(openSecondFrameworks, text = 'Massage')
serviceFacialLabel.grid(row = 6, column = 0)

serviceMassageCombo = ttk.Checkbutton(openSecondFrameworks, command = regular)
serviceMassageCombo.grid(row = 6, column = 1)

serviceMassageTypeLabel = tkinter.Label(openSecondFrameworks, text = 'Type: ')
serviceMassageTypeLabel.grid(row = 7, column = 0)

serviceMassageTypeCombo= ttk.Combobox(openSecondFrameworks, values = ['Full body', 'Thai', 'Hot stones', 'Chinese', 'Spa with body wrap'])
serviceMassageTypeCombo.grid(row = 7, column = 1)

serviceMassagePriceLabel = tkinter.Label(openSecondFrameworks, text = 'Price: ')
serviceMassagePriceLabel.grid(row = 7, column = 2)

serviceMassagePriceCombo= ttk.Combobox(openSecondFrameworks, values=[85.00, 50.00, 48.00, 55.00, 85.00])
serviceFacialPriceCombo.grid(row = 7, column = 3)

openThirdFrameworks = tkinter.LabelFrame(frame, fg ='green', text='Final info: ')
openThirdFrameworks.grid(row=2, column=0)

userDiscountLabel = tkinter.Label(openThirdFrameworks, text = 'Discount: ')
userDiscountLabel.grid(row = 2, column = 0)

userDiscountCombo= ttk.Combobox(openThirdFrameworks, values = ['5%', '10%', '15%'])
userDiscountCombo.grid(row = 2, column = 1)

userRegularLabel = tkinter.Label(openThirdFrameworks, text = 'Regular customer')
userRegularLabel.grid(row = 1, column = 0)

userRegular = ttk.Checkbutton(openThirdFrameworks, command = regular)
userRegular.grid(row = 1, column = 1)

userTotalPriceLabel = tkinter.Label(openThirdFrameworks, text = 'Total price: ')
userDiscountLabel.grid(row = 2, column = 0)

saveButton = tkinter.Button(frame, text='Save', command=save_button)
saveButton.grid(row=5, column=0)

printCheckButton = tkinter.Button(frame, text='Print check', activebackground='red', command=check_button)
printCheckButton.grid(row=6, column=0)

window.mainloop()
