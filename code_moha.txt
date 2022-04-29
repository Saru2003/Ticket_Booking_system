from tkinter import *
from tkinter.font import Font
from tkinter import messagebox
import random
import smtplib
from email.mime.text import MIMEText
def randletter(x, y):
    return chr(random.randint(ord(x), ord(y)))


R = randletter('A', 'G')
rand = (R)
r = rand
rr = str(random.randint(0, 10))
k = (r + rr)

root = Tk()
root.title("CineMagic")
root.geometry("1400x690")
var = StringVar()
var2 = StringVar()
var_3 = StringVar()
check1 = IntVar()
check1.set(0)
variable_1 = StringVar()
variable1 = StringVar()
variable2 = StringVar()
variable_1.set("0")
variable1.set("0")
variable2.set("0")
myfont = Font(family="Times New Roman", size=20, slant="italic")
myfont1 = Font(family="Courier", size=25, weight="bold")
myfont2 = Font(family="verdana", weight="bold")
myfont3 = Font(family="Garuda", weight="bold", underline=1, size=20)
myfont4 = Font(family="Nakula", slant="italic", size=15)
lalfont = Font(family="Times", size=25)
lalfonts = Font(family="Times", size=25, underline=2)
lalfontl = Font(family="Times", size=13)
classs=0
var5 = BooleanVar()
var6 = BooleanVar()
var7 = BooleanVar()
var8 = BooleanVar()
var9 = BooleanVar()
var10 = BooleanVar()
var11 = BooleanVar()
var12 = BooleanVar()
var13 = BooleanVar()
var14 = BooleanVar()
var15 = BooleanVar()
var16 = BooleanVar()
var17 = BooleanVar()
var18 = BooleanVar()
var19 = BooleanVar()
var20 = StringVar()
var21 = StringVar()
var22 = StringVar()
var23 = StringVar()
var4 = StringVar()
var3 = StringVar()
lol1 = var_3.get()
loldate = var3.get()
price = 0
ve = 0
y=0
date=0
overstrik = Font(family="Times", size=25, overstrike=1)
aa = Font(family="arial", size=20)
aa1 = Font(family="arial", size=15,weight="bold")
n = []
var__3=StringVar()
ab=Font(family="Times",size=15)
abb=Font(family="Times",size=17,weight="bold",underline=2)
ab_=Font(family="arial",size=13,slant="italic")
big=Font(family="loma",size=45,slant="italic")
def _open2():
    global price,varcombo,cc,y,n
    top = Toplevel()
    top.geometry("800x425")
    top.title("Food")
    top.configure(bg="black")
    varcombo=StringVar()
    if var_3.get() == "Platinum (A - C) : 350 Rs. ":
        price = 350
    if var_3.get() == "Normal (D - F) : 175 Rs. ":
        price = 175
    if var_3.get() == "Budget (G - J) : 115 Rs. ":
        price = 115
    def yes():
        global y
        y='yes'
        top.destroy()
    def no():
        n='no'
        top.destroy()
    byes=Button(top,text="APPLY",font=ab,width=10,bg="orange", fg="white",command=yes).place(x=375,y=295)
    bno=Button(top,text="CANCEL",font=ab,width=10,bg="orange", fg="white",command=no).place(x=500,y=295)
    bbx = Button(top, text="X", font="verdana", bg="orange", fg="white",command=top.destroy).place(x=780, y=2)
    
    o = Label(top, text="{}".format(price + 150), font=overstrik, fg="yellow", bg="black").place(x=427, y=200)
    op = Label(top, text="{}".format(price + 100), font=lalfont, bg="black", fg="yellow").place(x=495, y=200)
    lal1 = Label(top, text="An offer like never before!", font=lalfont, fg="yellow", bg="Black").place(x=185, y=50)
    t = Label(top,
              text="Ticket                                                   Food                                                          Offer Price",
              fg="yellow", bg="black").place(x=30, y=150)
    tick = Label(top, text="{}      +        150        =  ".format(price), font=lalfont, fg="yellow", bg="black")
    tick.place(x=30, y=200)
    top.mainloop()
def y_():
    mmovie=0
    date=0
    time=0
    month=0
    k=0
    if var5.get():
        mmovie="K.G.F"
    if var6.get():
        mmovie="Baahubali: The Beginning"
    if var7.get():
        mmovie="Baahubali 2: The Conclusion"
    if var8.get():
        mmovie="Bigil"
    if var9.get():
        mmovie="Petta"
    if var10.get():
        mmovie="Joker"
    if var11.get():
        mmovie="Inception"
    if var12.get():
        mmovie="Tag"
    if var13.get():
        mmovie="Indiana Jones"
    if var14.get():
        mmovie="Avatar"
    if var15.get():
        mmovie="Athiran"
    if var16.get():
        mmovie="Kireedam"
    if var17.get():
        mmovie="Mathilukal"
    if var18.get():
        mmovie="Helen"
    if var19.get():
        mmovie="Thondimuthalum Driksakshiyum"
    l="\nTERMS & CONDITIONS\n    1. You agree that your use of this Website and the purchase of any movie ticket, goods or services will be governed by these terms and conditions.\n    2. Movie tickets purchased via this Website are non-refundable and are not available for exchange, unless required by law.\n    3. Tickets once issued cannot be cancelled, exchanged or refunded. Show timings are subject to change.\n    4. 3D glass usage fee is non-refundable.\n    5. Patrons below 18 years of age will not be admitted to 'A' rated movies.\n    6. Children over 3 years of age require a ticket for entry into the screens.\n    7. Food order cannot be cancelled. Outside food will not be allowed inside the complex.\n    8. Smoking, consumption of alcohol and chewing of paan is strictly prohibited within the premises.\n    9. Intoxicated persons will not be admitted into the cinema.\n    10. Management will not be responsible for loss or damage of any personal property.\n    11. If a show is cancelled, the responsibility of Management is limited to the face value of the ticket.\n    12. Right of admission reserved.\n    13. All other CineMagic terms and conditions apply."
    if y=='yes':
          k=(int(f)*2)+(int(f)*17)+((100+price)*int(f))
    else:
          k=((int(f)*price)+(int(f)*17)+(int(f)*2))
    amt=str(30*int(f))
    amt_=str(k)
    amt__=str((k)+(30*int(f)))

    zz=var3.get()+" "+var4.get()+" ,"+var__3.get()
    if a=="y":
        body="                                   CineMagic\n"+"Dear "+e1+" \n"+"Here are the details of your ticket booking with CineMagic.\n"+"       Movie:   "+mmovie+"\n       Show Date, Time:   "+zz+"\n       Class:   "+classs+"\n       Seat No(s):   "
        for i in l2:
            body+=" %s"%(i)
        fromx = 'sarvesh20123@gmail.com'
        to  = e2
        i=body+"\n       Cinema: "+var.get()+"\nBILLING"+"\n       No. of ticktes:   "+f+"\n       Ticket Booking Charge:   Rs. "+amt+" (Rs 30 per Ticket)"+"\n       Ticket Amount:   Rs. "+amt_+" (Including conv.fees, GST)"+"\n       Total Amount:   Rs. "+amt__+l+"\nThank you for choosing CineMagic. See you at the movies!"
        msg = MIMEText(i)
        msg['Subject'] = 'Tickets info'
        msg['From'] = fromx
        msg['To'] = to

        server = smtplib.SMTP('smtp.gmail.com:587')
        server.starttls()
        server.ehlo()
        server.login('sarvesh20123@gmail.com', 'A1.2.3.4.5.6')
        server.sendmail(fromx, to, msg.as_string())
        server.quit()
        print("Successfully sent! Thank you.")
    else:
        print("Thank you.")

ve = 0
e=StringVar()
e_=StringVar()
e_1=StringVar()
def another1():
    global var__3,classs
    top = Toplevel()
    top.geometry("1400x690")
    ve = 0
    if var_3.get() == "Platinum (A - C) : 350 Rs. ":
        price = 350
    if var_3.get() == "Normal (D - F) : 175 Rs. ":
        price = 175
    if var_3.get() == "Budget (G - J) : 115 Rs. ":
        price = 115
    def l():
        global a,e2,e1
        top.destroy()
        messagebox.showinfo("CineMagic", "Successfully Booked")
        e1=e.get()
        e2=e_.get()
        e3=e_1.get()
        print("               {}           A/C   ".format(var.get()))
        print(var3.get(),var4.get()," ",var__3.get())
        print("Name: ",e1)
        print("E-Mail: ",e2)
        print("Phone: ",e3)
        print("Tickets: ",l2)
        print("")
        root.destroy()
        a=input("Do you want a soft copy to be sent to your mail? (y/n) ")
        y_()
    if var_3.get()=="Platinum (A - C) : 350 Rs. ":
           classs="Platinum"
           for i in range(int(f)):
              R = randletter('A', 'C')
              rand = (R)  
              z = rand
              rr = str(random.randint(1, 30))
              k = (R + rr)
              l2.append(str(k))
    if var_3.get()=="Normal (D - F) : 175 Rs. ":
           classs="Normal"
           for i in range(int(f)):
              R = randletter('D', 'F')
              rand = (R)  
              z = rand
              rr = str(random.randint(1, 30))
              k = (R + rr)
              l2.append(str(k))
    if var_3.get()=="Budget (G - J) : 115 Rs. ":
           classs="Budget"
           for i in range(int(f)):
              R = randletter('D', 'F')
              rand = (R)  
              z = rand
              rr = str(random.randint(1, 30))
              k = (R + rr)
              l2.append(str(k))
    a1 = Label(top, text="YOUR CONTACT DETAILS", font=lalfonts).place(x=2, y=1)
    name1 = Label(top, text="NAME:", font=lalfontl).place(x=50, y=46)
    entryname = Entry(top, width=20, font="verdana",borderwidth=4,textvariable=e).place(x=50, y=75)
    email = Label(top, text="E-MAIL:", font=lalfontl).place(x=275, y=46)
    entrymail = Entry(top, width=21, font="verdana",borderwidth=4,textvariable=e_).place(x=275, y=75)
    phone = Label(top, text="PHONE:", font=lalfontl).place(x=500, y=46)
    phone1 = Entry(top, width=20, font="verdana",borderwidth=4,textvariable=e_1).place(x=500, y=75)
    if (var5.get()):
        kgff = Label(top, text="K.G.F (2D)", font=aa).place(x=900, y=20)
        kgff1 = Label(top, text="{}".format(var.get()), font="verdana").place(x=900, y=80)
        kgfff2 = Label(top, text=f"on {var3.get()}",font="verdana").place(x=900, y=190)
        kgfff_2 = Label(top, text=f"{var4.get()}",font="verdana").place(x=950, y=190)
        time = ["9.00 am - 12.00 am", "1.00 pm - 4 pm ", "4.30 pm - 7.30 pm","10.00 pm - 2.00 pm"]
        droptype = OptionMenu(top, var__3, *time)
        var__3.set("Select Timings")
        droptype.config(bg="#263D42", fg="white",font="verdana")
        droptype.place(x=1095,y=180)
        kgfff3 = Label(top, text="SEAT INFO", font=aa).place(x=900, y=144)
        if y=='yes':
          kgfff4= Label(top,text="{} seats                   {} INR".format(f,((100+(price))*int(f))),font="verdana").place(x=900,y=260)
          kgfff5=Label(top,text="Conv. fees                 {} INR".format(int(f)*17),font="verdana").place(x=900,y=285)
          kgfff6=Label(top,text="GST                           {} INR".format(int(f)*2),font="verdana").place(x=900,y=310)
          kgfff7=Label(top,text="TOTAL                         {}".format((int(f)*2)+(int(f)*17)+((100+price)*int(f))),font=aa1).place(x=900,y=375)
        else:
          kgfff4= Label(top,text="{} seats                   {} INR".format(f,int(f)*price),font="verdana").place(x=900,y=260)
          kgfff5=Label(top,text="Conv. fees                 {} INR".format(int(f)*17),font="verdana").place(x=900,y=285)
          kgfff6=Label(top,text="GST                           {} INR".format(int(f)*2),font="verdana").place(x=900,y=310)
          kgfff7=Label(top,text="TOTAL                         {}".format((int(f)*price)+(int(f)*17)+(int(f)*2)),font=aa1).place(x=900,y=375)
    if (var6.get()):
        kgff = Label(top, text="Baahubali: The Beginning (2D)", font=aa).place(x=900, y=20)
        kgff1 = Label(top, text="{}".format(var.get()), font="verdana").place(x=900, y=80)
        kgfff2 = Label(top, text=f"on {var3.get()}",font="verdana").place(x=900, y=190)
        kgfff_2 = Label(top, text=f"{var4.get()}",font="verdana").place(x=950, y=190)
        time = ["9.00 am - 12.00 am", "1.00 pm - 4 pm ", "4.30 pm - 7.30 pm","10.00 pm - 2.00 pm"]
        droptype = OptionMenu(top, var__3, *time)
        var__3.set("Select Timings")
        droptype.config(bg="#263D42", fg="white",font="verdana")
        droptype.place(x=1095,y=180)
        kgfff3 = Label(top, text="SEAT INFO", font=aa).place(x=900, y=144)
        if y=='yes':
          kgfff4= Label(top,text="{} seats                   {} INR".format(f,((100+price)*int(f))),font="verdana").place(x=900,y=260)
          kgfff5=Label(top,text="Conv. fees                 {} INR".format(int(f)*17),font="verdana").place(x=900,y=285)
          kgfff6=Label(top,text="GST                           {} INR".format(int(f)*2),font="verdana").place(x=900,y=310)
          kgfff7=Label(top,text="TOTAL                         {}".format((int(f)*2)+(int(f)*17)+((100+price)*int(f))),font=aa1).place(x=900,y=375)
        else:
          kgfff4= Label(top,text="{} seats                   {} INR".format(f,int(f)*price),font="verdana").place(x=900,y=260)
          kgfff5=Label(top,text="Conv. fees                 {} INR".format(int(f)*17),font="verdana").place(x=900,y=285)
          kgfff6=Label(top,text="GST                           {} INR".format(int(f)*2),font="verdana").place(x=900,y=310)
          kgfff7=Label(top,text="TOTAL                         {}".format((int(f)*price)+(int(f)*17)+(int(f)*2)),font=aa1).place(x=900,y=375)
    if (var7.get()):
        kgff = Label(top, text="Baahubali: The Conclusion (2D)", font=aa).place(x=900, y=20)
        kgff1 = Label(top, text="{}".format(var.get()), font="verdana").place(x=900, y=80)
        kgfff2 = Label(top, text=f"on {var3.get()}",font="verdana").place(x=900, y=190)
        kgfff_2 = Label(top, text=f"{var4.get()}",font="verdana").place(x=950, y=190)
        time = ["9.00 am - 12.00 am", "1.00 pm - 4 pm ", "4.30 pm - 7.30 pm","10.00 pm - 2.00 pm"]
        droptype = OptionMenu(top, var__3, *time)
        var__3.set("Select Timings")
        droptype.config(bg="#263D42", fg="white",font="verdana")
        droptype.place(x=1095,y=180)
        kgfff3 = Label(top, text="SEAT INFO", font=aa).place(x=900, y=144)
        if y=='yes':
          kgfff4= Label(top,text="{} seats                   {} INR".format(f,((100+price)*int(f))),font="verdana").place(x=900,y=260)
          kgfff5=Label(top,text="Conv. fees                 {} INR".format(int(f)*17),font="verdana").place(x=900,y=285)
          kgfff6=Label(top,text="GST                           {} INR".format(int(f)*2),font="verdana").place(x=900,y=310)
          kgfff7=Label(top,text="TOTAL                         {}".format((int(f)*2)+(int(f)*17)+((100+price)*int(f))),font=aa1).place(x=900,y=375)
        else:
          kgfff4= Label(top,text="{} seats                   {} INR".format(f,int(f)*price),font="verdana").place(x=900,y=260)
          kgfff5=Label(top,text="Conv. fees                 {} INR".format(int(f)*17),font="verdana").place(x=900,y=285)
          kgfff6=Label(top,text="GST                           {} INR".format(int(f)*2),font="verdana").place(x=900,y=310)
          kgfff7=Label(top,text="TOTAL                         {}".format((int(f)*price)+(int(f)*17)+(int(f)*2)),font=aa1).place(x=900,y=375)
    if (var9.get()):
        kgff = Label(top, text=" Bigil (2D)", font=aa).place(x=900, y=20)
        kgff1 = Label(top, text="{}".format(var.get()), font="verdana").place(x=900, y=80)
        kgfff2 = Label(top, text=f"on {var3.get()}",font="verdana").place(x=900, y=190)
        kgfff_2 = Label(top, text=f"{var4.get()}",font="verdana").place(x=950, y=190)
        time = ["9.00 am - 12.00 am", "1.00 pm - 4 pm ", "4.30 pm - 7.30 pm","10.00 pm - 2.00 pm"]
        droptype = OptionMenu(top, var__3, *time)
        var__3.set("Select Timings")
        droptype.config(bg="#263D42", fg="white",font="verdana")
        droptype.place(x=1095,y=180)
        kgfff3 = Label(top, text="SEAT INFO", font=aa).place(x=900, y=144)
        if y=='yes':
          kgfff4= Label(top,text="{} seats                   {} INR".format(f,((100+price)*int(f))),font="verdana").place(x=900,y=260)
          kgfff5=Label(top,text="Conv. fees                 {} INR".format(int(f)*17),font="verdana").place(x=900,y=285)
          kgfff6=Label(top,text="GST                           {} INR".format(int(f)*2),font="verdana").place(x=900,y=310)
          kgfff7=Label(top,text="TOTAL                         {}".format((int(f)*2)+(int(f)*17)+((100+price)*int(f))),font=aa1).place(x=900,y=375)
        else:
          kgfff4= Label(top,text="{} seats                   {} INR".format(f,int(f)*price),font="verdana").place(x=900,y=260)
          kgfff5=Label(top,text="Conv. fees                 {} INR".format(int(f)*17),font="verdana").place(x=900,y=285)
          kgfff6=Label(top,text="GST                           {} INR".format(int(f)*2),font="verdana").place(x=900,y=310)
          kgfff7=Label(top,text="TOTAL                         {}".format((int(f)*price)+(int(f)*17)+(int(f)*2)),font=aa1).place(x=900,y=375)
    if (var8.get()):
        kgff = Label(top, text="Petta (2D)", font=aa).place(x=900, y=20)
        kgff1 = Label(top, text="{}".format(var.get()), font="verdana").place(x=900, y=80)
        kgfff2 = Label(top, text=f"on {var3.get()}",font="verdana").place(x=900, y=190)
        kgfff_2 = Label(top, text=f"{var4.get()}",font="verdana").place(x=950, y=190)
        time = ["9.00 am - 12.00 am", "1.00 pm - 4 pm ", "4.30 pm - 7.30 pm","10.00 pm - 2.00 pm"]
        droptype = OptionMenu(top, var__3, *time)
        var__3.set("Select Timings")
        droptype.config(bg="#263D42", fg="white",font="verdana")
        droptype.place(x=1095,y=180)
        kgfff3 = Label(top, text="SEAT INFO", font=aa).place(x=900, y=144)
        if y=='yes':
          kgfff4= Label(top,text="{} seats                   {} INR".format(f,((100+price)*int(f))),font="verdana").place(x=900,y=260)
          kgfff5=Label(top,text="Conv. fees                 {} INR".format(int(f)*17),font="verdana").place(x=900,y=285)
          kgfff6=Label(top,text="GST                           {} INR".format(int(f)*2),font="verdana").place(x=900,y=310)
          kgfff7=Label(top,text="TOTAL                         {}".format((int(f)*2)+(int(f)*17)+((100+price)*int(f))),font=aa1).place(x=900,y=375)
        else:
          kgfff4= Label(top,text="{} seats                   {} INR".format(f,int(f)*price),font="verdana").place(x=900,y=260)
          kgfff5=Label(top,text="Conv. fees                 {} INR".format(int(f)*17),font="verdana").place(x=900,y=285)
          kgfff6=Label(top,text="GST                           {} INR".format(int(f)*2),font="verdana").place(x=900,y=310)
          kgfff7=Label(top,text="TOTAL                         {}".format((int(f)*price)+(int(f)*17)+(int(f)*2)),font=aa1).place(x=900,y=375)
    if (var10.get()):
        kgff = Label(top, text="Joker (2D)", font=aa).place(x=900, y=20)
        kgff1 = Label(top, text="{}".format(var.get()), font="verdana").place(x=900, y=80)
        kgfff2 = Label(top, text=f"on {var3.get()}",font="verdana").place(x=900, y=190)
        kgfff_2 = Label(top, text=f"{var4.get()}",font="verdana").place(x=950, y=190)
        time = ["9.00 am - 12.00 am", "1.00 pm - 4 pm ", "4.30 pm - 7.30 pm","10.00 pm - 2.00 pm"]
        droptype = OptionMenu(top, var__3, *time)
        var__3.set("Select Timings")
        droptype.config(bg="#263D42", fg="white",font="verdana")
        droptype.place(x=1095,y=180)
        kgfff3 = Label(top, text="SEAT INFO", font=aa).place(x=900, y=144)
        if y=='yes':
          kgfff4= Label(top,text="{} seats                   {} INR".format(f,((100+price)*int(f))),font="verdana").place(x=900,y=260)
          kgfff5=Label(top,text="Conv. fees                 {} INR".format(int(f)*17),font="verdana").place(x=900,y=285)
          kgfff6=Label(top,text="GST                           {} INR".format(int(f)*2),font="verdana").place(x=900,y=310)
          kgfff7=Label(top,text="TOTAL                         {}".format((int(f)*2)+(int(f)*17)+((100+price)*int(f))),font=aa1).place(x=900,y=375)
        else:
          kgfff4= Label(top,text="{} seats                   {} INR".format(f,int(f)*price),font="verdana").place(x=900,y=260)
          kgfff5=Label(top,text="Conv. fees                 {} INR".format(int(f)*17),font="verdana").place(x=900,y=285)
          kgfff6=Label(top,text="GST                           {} INR".format(int(f)*2),font="verdana").place(x=900,y=310)
          kgfff7=Label(top,text="TOTAL                         {}".format((int(f)*price)+(int(f)*17)+(int(f)*2)),font=aa1).place(x=900,y=375)
    if (var11.get()):
        kgff = Label(top, text="Inception (2D)", font=aa).place(x=900, y=20)
        kgff1 = Label(top, text="{}".format(var.get()), font="verdana").place(x=900, y=80)
        kgfff2 = Label(top, text=f"on {var3.get()}",font="verdana").place(x=900, y=190)
        kgfff_2 = Label(top, text=f"{var4.get()}",font="verdana").place(x=950, y=190)
        time = ["9.00 am - 12.00 am", "1.00 pm - 4 pm ", "4.30 pm - 7.30 pm","10.00 pm - 2.00 pm"]
        droptype = OptionMenu(top, var__3, *time)
        var__3.set("Select Timings")
        droptype.config(bg="#263D42", fg="white",font="verdana")
        droptype.place(x=1095,y=180)
        kgfff3 = Label(top, text="SEAT INFO", font=aa).place(x=900, y=144)
        if y=='yes':
          kgfff4= Label(top,text="{} seats                   {} INR".format(f,((100+price)*int(f))),font="verdana").place(x=900,y=260)
          kgfff5=Label(top,text="Conv. fees                 {} INR".format(int(f)*17),font="verdana").place(x=900,y=285)
          kgfff6=Label(top,text="GST                           {} INR".format(int(f)*2),font="verdana").place(x=900,y=310)
          kgfff7=Label(top,text="TOTAL                         {}".format((int(f)*2)+(int(f)*17)+((100+price)*int(f))),font=aa1).place(x=900,y=375)
        else:
          kgfff4= Label(top,text="{} seats                   {} INR".format(f,int(f)*price),font="verdana").place(x=900,y=260)
          kgfff5=Label(top,text="Conv. fees                 {} INR".format(int(f)*17),font="verdana").place(x=900,y=285)
          kgfff6=Label(top,text="GST                           {} INR".format(int(f)*2),font="verdana").place(x=900,y=310)
          kgfff7=Label(top,text="TOTAL                         {}".format((int(f)*price)+(int(f)*17)+(int(f)*2)),font=aa1).place(x=900,y=375)
    if (var12.get()):
        kgff = Label(top, text="Tag (2D)", font=aa).place(x=900, y=20)
        kgff1 = Label(top, text="{}".format(var.get()), font="verdana").place(x=900, y=80)
        kgfff2 = Label(top, text=f"on {var3.get()}",font="verdana").place(x=900, y=190)
        kgfff_2 = Label(top, text=f"{var4.get()}",font="verdana").place(x=950, y=190)
        time = ["9.00 am - 12.00 am", "1.00 pm - 4 pm ", "4.30 pm - 7.30 pm","10.00 pm - 2.00 pm"]
        droptype = OptionMenu(top, var__3, *time)
        var__3.set("Select Timings")
        droptype.config(bg="#263D42", fg="white",font="verdana")
        droptype.place(x=1095,y=180)
        kgfff3 = Label(top, text="SEAT INFO", font=aa).place(x=900, y=144)
        if y=='yes':
          kgfff4= Label(top,text="{} seats                   {} INR".format(f,((100+price)*int(f))),font="verdana").place(x=900,y=260)
          kgfff5=Label(top,text="Conv. fees                 {} INR".format(int(f)*17),font="verdana").place(x=900,y=285)
          kgfff6=Label(top,text="GST                           {} INR".format(int(f)*2),font="verdana").place(x=900,y=310)
          kgfff7=Label(top,text="TOTAL                         {}".format((int(f)*2)+(int(f)*17)+((100+price)*int(f))),font=aa1).place(x=900,y=375)
        else:
          kgfff4= Label(top,text="{} seats                   {} INR".format(f,int(f)*price),font="verdana").place(x=900,y=260)
          kgfff5=Label(top,text="Conv. fees                 {} INR".format(int(f)*17),font="verdana").place(x=900,y=285)
          kgfff6=Label(top,text="GST                           {} INR".format(int(f)*2),font="verdana").place(x=900,y=310)
          kgfff7=Label(top,text="TOTAL                         {}".format((int(f)*price)+(int(f)*17)+(int(f)*2)),font=aa1).place(x=900,y=375)
    if (var13.get()):
        kgff = Label(top, text="Indiana Jones (2D)", font=aa).place(x=900, y=20)
        kgff1 = Label(top, text="{}".format(var.get()), font="verdana").place(x=900, y=80)
        kgfff2 = Label(top, text=f"on {var3.get()}",font="verdana").place(x=900, y=190)
        kgfff_2 = Label(top, text=f"{var4.get()}",font="verdana").place(x=950, y=190)
        time = ["9.00 am - 12.00 am", "1.00 pm - 4 pm ", "4.30 pm - 7.30 pm","10.00 pm - 2.00 pm"]
        droptype = OptionMenu(top, var__3, *time)
        var__3.set("Select Timings")
        droptype.config(bg="#263D42", fg="white",font="verdana")
        droptype.place(x=1095,y=180)
        kgfff3 = Label(top, text="SEAT INFO", font=aa).place(x=900, y=144)
        if y=='yes':
          kgfff4= Label(top,text="{} seats                   {} INR".format(f,((100+price)*int(f))),font="verdana").place(x=900,y=260)
          kgfff5=Label(top,text="Conv. fees                 {} INR".format(int(f)*17),font="verdana").place(x=900,y=285)
          kgfff6=Label(top,text="GST                           {} INR".format(int(f)*2),font="verdana").place(x=900,y=310)
          kgfff7=Label(top,text="TOTAL                         {}".format((int(f)*2)+(int(f)*17)+((100+price)*int(f))),font=aa1).place(x=900,y=375)
        else:
          kgfff4= Label(top,text="{} seats                   {} INR".format(f,int(f)*price),font="verdana").place(x=900,y=260)
          kgfff5=Label(top,text="Conv. fees                 {} INR".format(int(f)*17),font="verdana").place(x=900,y=285)
          kgfff6=Label(top,text="GST                           {} INR".format(int(f)*2),font="verdana").place(x=900,y=310)
          kgfff7=Label(top,text="TOTAL                         {}".format((int(f)*price)+(int(f)*17)+(int(f)*2)),font=aa1).place(x=900,y=375)
    if (var14.get()):
        kgff = Label(top, text="Avatar [3D]", font=aa).place(x=900, y=20)
        kgff1 = Label(top, text="{}".format(var.get()), font="verdana").place(x=900, y=80)
        kgfff2 = Label(top, text=f"on {var3.get()}",font="verdana").place(x=900, y=190)
        kgfff_2 = Label(top, text=f"{var4.get()}",font="verdana").place(x=950, y=190)
        time = ["9.00 am - 12.00 am", "1.00 pm - 4 pm ", "4.30 pm - 7.30 pm","10.00 pm - 2.00 pm"]
        droptype = OptionMenu(top, var__3, *time)
        var__3.set("Select Timings")
        droptype.config(bg="#263D42", fg="white",font="verdana")
        droptype.place(x=1095,y=180)
        kgfff3 = Label(top, text="SEAT INFO", font=aa).place(x=900, y=144)
        if y=='yes':
          kgfff4= Label(top,text="{} seats                   {} INR".format(f,((100+price)*int(f))),font="verdana").place(x=900,y=260)
          kgfff5=Label(top,text="Conv. fees                 {} INR".format(int(f)*17),font="verdana").place(x=900,y=285)
          kgfff6=Label(top,text="GST                           {} INR".format(int(f)*2),font="verdana").place(x=900,y=310)
          kgfff7=Label(top,text="TOTAL                         {}".format((int(f)*2)+(int(f)*17)+((100+price)*int(f))),font=aa1).place(x=900,y=375)
        else:
          kgfff4= Label(top,text="{} seats                   {} INR".format(f,int(f)*price),font="verdana").place(x=900,y=260)
          kgfff5=Label(top,text="Conv. fees                 {} INR".format(int(f)*17),font="verdana").place(x=900,y=285)
          kgfff6=Label(top,text="GST                           {} INR".format(int(f)*2),font="verdana").place(x=900,y=310)
          kgfff7=Label(top,text="TOTAL                         {}".format((int(f)*price)+(int(f)*17)+(int(f)*2)),font=aa1).place(x=900,y=375)
    if (var15.get()):
        kgff = Label(top, text="Athiran (2D)", font=aa).place(x=900, y=20)
        kgff1 = Label(top, text="{}".format(var.get()), font="verdana").place(x=900, y=80)
        kgfff2 = Label(top, text=f"on {var3.get()}",font="verdana").place(x=900, y=190)
        kgfff_2 = Label(top, text=f"{var4.get()}",font="verdana").place(x=950, y=190)
        time = ["9.00 am - 12.00 am", "1.00 pm - 4 pm ", "4.30 pm - 7.30 pm","10.00 pm - 2.00 pm"]
        droptype = OptionMenu(top, var__3, *time)
        var__3.set("Select Timings")
        droptype.config(bg="#263D42", fg="white",font="verdana")
        droptype.place(x=1095,y=180)
        kgfff3 = Label(top, text="SEAT INFO", font=aa).place(x=900, y=144)
        if y=='yes':
          kgfff4= Label(top,text="{} seats                   {} INR".format(f,((100+price)*int(f))),font="verdana").place(x=900,y=260)
          kgfff5=Label(top,text="Conv. fees                 {} INR".format(int(f)*17),font="verdana").place(x=900,y=285)
          kgfff6=Label(top,text="GST                           {} INR".format(int(f)*2),font="verdana").place(x=900,y=310)
          kgfff7=Label(top,text="TOTAL                         {}".format((int(f)*2)+(int(f)*17)+((100+price)*int(f))),font=aa1).place(x=900,y=375)
        else:
          kgfff4= Label(top,text="{} seats                   {} INR".format(f,int(f)*price),font="verdana").place(x=900,y=260)
          kgfff5=Label(top,text="Conv. fees                 {} INR".format(int(f)*17),font="verdana").place(x=900,y=285)
          kgfff6=Label(top,text="GST                           {} INR".format(int(f)*2),font="verdana").place(x=900,y=310)
          kgfff7=Label(top,text="TOTAL                         {}".format((int(f)*price)+(int(f)*17)+(int(f)*2)),font=aa1).place(x=900,y=375)
    if (var16.get()):
        kgff = Label(top, text="Kireedam (2D)", font=aa).place(x=900, y=20)
        kgff1 = Label(top, text="{}".format(var.get()), font="verdana").place(x=900, y=80)
        kgfff2 = Label(top, text=f"on {var3.get()}",font="verdana").place(x=900, y=190)
        kgfff_2 = Label(top, text=f"{var4.get()}",font="verdana").place(x=950, y=190)
        time = ["9.00 am - 12.00 am", "1.00 pm - 4 pm ", "4.30 pm - 7.30 pm","10.00 pm - 2.00 pm"]
        droptype = OptionMenu(top, var__3, *time)
        var__3.set("Select Timings")
        droptype.config(bg="#263D42", fg="white",font="verdana")
        droptype.place(x=1095,y=180)
        kgfff3 = Label(top, text="SEAT INFO", font=aa).place(x=900, y=144)
        if y=='yes':
          kgfff4= Label(top,text="{} seats                   {} INR".format(f,((100+price)*int(f))),font="verdana").place(x=900,y=260)
          kgfff5=Label(top,text="Conv. fees                 {} INR".format(int(f)*17),font="verdana").place(x=900,y=285)
          kgfff6=Label(top,text="GST                           {} INR".format(int(f)*2),font="verdana").place(x=900,y=310)
          kgfff7=Label(top,text="TOTAL                         {}".format((int(f)*2)+(int(f)*17)+((100+price)*int(f))),font=aa1).place(x=900,y=375)
        else:
          kgfff4= Label(top,text="{} seats                   {} INR".format(f,int(f)*price),font="verdana").place(x=900,y=260)
          kgfff5=Label(top,text="Conv. fees                 {} INR".format(int(f)*17),font="verdana").place(x=900,y=285)
          kgfff6=Label(top,text="GST                           {} INR".format(int(f)*2),font="verdana").place(x=900,y=310)
          kgfff7=Label(top,text="TOTAL                         {}".format((int(f)*price)+(int(f)*17)+(int(f)*2)),font=aa1).place(x=900,y=375)
    if (var17.get()):
        kgff = Label(top, text="Mathilukal (2D)", font=aa).place(x=900, y=20)
        kgff1 = Label(top, text="{}".format(var.get()), font="verdana").place(x=900, y=80)
        kgfff2 = Label(top, text=f"on {var3.get()}",font="verdana").place(x=900, y=190)
        kgfff_2 = Label(top, text=f"{var4.get()}",font="verdana").place(x=950, y=190)
        time = ["9.00 am - 12.00 am", "1.00 pm - 4 pm ", "4.30 pm - 7.30 pm","10.00 pm - 2.00 pm"]
        droptype = OptionMenu(top, var__3, *time)
        var__3.set("Select Timings")
        droptype.config(bg="#263D42", fg="white",font="verdana")
        droptype.place(x=1095,y=180)
        kgfff3 = Label(top, text="SEAT INFO", font=aa).place(x=900, y=144)
        if y=='yes':
          kgfff4= Label(top,text="{} seats                   {} INR".format(f,((100+price)*int(f))),font="verdana").place(x=900,y=260)
          kgfff5=Label(top,text="Conv. fees                 {} INR".format(int(f)*17),font="verdana").place(x=900,y=285)
          kgfff6=Label(top,text="GST                           {} INR".format(int(f)*2),font="verdana").place(x=900,y=310)
          kgfff7=Label(top,text="TOTAL                         {}".format((int(f)*2)+(int(f)*17)+((100+price)*int(f))),font=aa1).place(x=900,y=375)
        else:
          kgfff4= Label(top,text="{} seats                   {} INR".format(f,int(f)*price),font="verdana").place(x=900,y=260)
          kgfff5=Label(top,text="Conv. fees                 {} INR".format(int(f)*17),font="verdana").place(x=900,y=285)
          kgfff6=Label(top,text="GST                           {} INR".format(int(f)*2),font="verdana").place(x=900,y=310)
          kgfff7=Label(top,text="TOTAL                         {}".format((int(f)*price)+(int(f)*17)+(int(f)*2)),font=aa1).place(x=900,y=375)
    if (var18.get()):
        kgff = Label(top, text="Helen (2D)", font=aa).place(x=900, y=20)
        kgff1 = Label(top, text="{}".format(var.get()), font="verdana").place(x=900, y=80)
        kgfff2 = Label(top, text=f"on {var3.get()}",font="verdana").place(x=900, y=190)
        kgfff_2 = Label(top, text=f"{var4.get()}",font="verdana").place(x=950, y=190)
        time = ["9.00 am - 12.00 am", "1.00 pm - 4 pm ", "4.30 pm - 7.30 pm","10.00 pm - 2.00 pm"]
        droptype = OptionMenu(top, var__3, *time)
        var__3.set("Select Timings")
        droptype.config(bg="#263D42", fg="white",font="verdana")
        droptype.place(x=1095,y=180)
        kgfff3 = Label(top, text="SEAT INFO", font=aa).place(x=900, y=144)
        if y=='yes':
          kgfff4= Label(top,text="{} seats                   {} INR".format(f,((100+price)*int(f))),font="verdana").place(x=900,y=260)
          kgfff5=Label(top,text="Conv. fees                 {} INR".format(int(f)*17),font="verdana").place(x=900,y=285)
          kgfff6=Label(top,text="GST                           {} INR".format(int(f)*2),font="verdana").place(x=900,y=310)
          kgfff7=Label(top,text="TOTAL                         {}".format((int(f)*2)+(int(f)*17)+((100+price)*int(f))),font=aa1).place(x=900,y=375)
        else:
          kgfff4= Label(top,text="{} seats                   {} INR".format(f,int(f)*price),font="verdana").place(x=900,y=260)
          kgfff5=Label(top,text="Conv. fees                 {} INR".format(int(f)*17),font="verdana").place(x=900,y=285)
          kgfff6=Label(top,text="GST                           {} INR".format(int(f)*2),font="verdana").place(x=900,y=310)
          kgfff7=Label(top,text="TOTAL                         {}".format((int(f)*price)+(int(f)*17)+(int(f)*2)),font=aa1).place(x=900,y=375)
    if (var19.get()):
        kgff = Label(top, text="Thondimuthalum Driksakshiyum (2D)", font=aa).place(x=900, y=20)
        kgff1 = Label(top, text="{}".format(var.get()), font="verdana").place(x=900, y=80)
        kgfff2 = Label(top, text=f"on {var3.get()}",font="verdana").place(x=900, y=190)
        kgfff_2 = Label(top, text=f"{var4.get()}",font="verdana").place(x=950, y=190)
        time = ["9.00 am - 12.00 am", "1.00 pm - 4 pm ", "4.30 pm - 7.30 pm","10.00 pm - 2.00 pm"]
        droptype = OptionMenu(top, var__3, *time)
        var__3.set("Select Timings")
        droptype.config(bg="#263D42", fg="white",font="verdana")
        droptype.place(x=1095,y=180)
        kgfff3 = Label(top, text="SEAT INFO", font=aa).place(x=900, y=144)
        if y=='yes':
          kgfff4= Label(top,text="{} seats                   {} INR".format(f,((100+price)*int(f))),font="verdana").place(x=900,y=260)
          kgfff5=Label(top,text="Conv. fees                 {} INR".format(int(f)*17),font="verdana").place(x=900,y=285)
          kgfff6=Label(top,text="GST                           {} INR".format(int(f)*2),font="verdana").place(x=900,y=310)
          kgfff7=Label(top,text="TOTAL                         {}".format((int(f)*2)+(int(f)*17)+((100+price)*int(f))),font=aa1).place(x=900,y=375)
        else:
          kgfff4= Label(top,text="{} seats                   {} INR".format(f,int(f)*price),font="verdana").place(x=900,y=260)
          kgfff5=Label(top,text="Conv. fees                 {} INR".format(int(f)*17),font="verdana").place(x=900,y=285)
          kgfff6=Label(top,text="GST                           {} INR".format(int(f)*2),font="verdana").place(x=900,y=310)
          kgfff7=Label(top,text="TOTAL                         {}".format((int(f)*price)+(int(f)*17)+(int(f)*2)),font=aa1).place(x=900,y=375)
    thankyou=Label(top,text="Thank You \n       \n  Visit Again..",font=big,fg="blue").place(x=90,y=200)
    btnn = Button(top, text="Proceed..",font="times",bg="#263D42", fg="white", width=20,height=2,command=l).place(x=920, y=475)
    top.mainloop()


def _open():
   global ver, v, var_3
   frame2.destroy()
   top = Toplevel(root)
   top.title("Book you tickets")
   top.geometry("1400x690")

   def _topdestroy():
        top.destroy()
        another1()
                
   def seat_select(val):
        global f, l2,var_3
        l2= []
        f = val
    
   if (var5.get()):
        kgf = Label(top, text="K.G.F (U/A)", font=("Times 32", 47)).place(x=20, y=10)
        kgf1 = Label(top, text="(U/A)   .   2h 37m   .   Tamil   .   Action/Drama", font=myfont2).place(x=20, y=90)
        kgf3 = Label(top, text="Synopsis:", font=myfont3).place(x=20, y=120)
        kgf4 = Label(top,
                     text="Rocky, a young man, seeks power and wealth in order to \nfulfil a promise to his dying mother. His quest takes him to\n Mumbai, where he gets involved with the notorious gold mafia.",
                     font=myfont4).place(x=0, y=157)
        kgf5 = Label(top, text="Cast:", font=myfont3).place(x=20, y=243)
        kgf6 = Label(top, text="Yash \nSrinidhi Shetty \nAnanth Nag \nRamachandra Raju \nAchyuth Kumar",
                     font=myfont4).place(x=15, y=280)
        kgf7 = Label(top, text="Cast Crew:", font=myfont3).place(x=20, y=415)
        kgf_7 = Label(top,
                      text="Directed by  Prashanth Neel\nProduced by  Vijay Kiragandur\nWritten by  Prashanth Neel, Chandramouli M, Vinay Shivangi\nScreenplay by  Prashanth Neel\nStory by    Prashanth Neel",
                      font=myfont4).place(x=0, y=455)

        kgfr = Label(top, text="Select number of tickets:", font=("Verdana", 12)).place(x=700, y=29)
        check = Checkbutton(top, text="Check this if you prefer corner seats").place(x=790, y=60)
        cineformat = Label(top, text="Cinema Class           :", font="Verdana").place(x=700, y=150)
        opt = ["Platinum (A - C) : 350 Rs. ", "Normal (D - F) : 175 Rs. ", "Budget (G - J) : 115 Rs. "]
        droptype = OptionMenu(top, var_3, *opt)
        var_3.set("Select")
        droptype.config(width=33, bg="#263D42", fg="white")
        droptype.place(x=920, y=150)
        ver = Scale(top, from_=0, to=20, orient=HORIZONTAL,command=seat_select).place(x=920,y=17)
        click = Button(top, text="Click here for EXCITING COMBO OFFERS!!", font="verdana", bg="#263D42", fg="white",
                       width=42, height=3, command=_open2).place(x=810, y=250)
        click2 = Button(top, text="Or click here to proceed", font='arial', bg="#263D42", fg="white", width=42,
                        command=_topdestroy).place(x=810, y=335)
   if (var6.get()):
        kgf = Label(top, text="Baahubali: The Beginning (U/A)", font=("Times 32", 47)).place(x=20, y=10)
        kgf1 = Label(top, text="(U/A)   .   2h 39m   .   Tamil   .   Action/War", font=myfont2).place(x=20, y=90)
        kgf3 = Label(top, text="Synopsis:", font=myfont3).place(x=20, y=120)
        kgf4 = Label(top,
                     text="In the kingdom of Mahishmati, Shivudu falls in love \nwith a young warrior woman. While trying to woo her, he learns about\n the conflict-ridden past of his family and his true legacy.",
                     font=myfont4).place(x=0, y=157)
        kgf5 = Label(top, text="Cast:", font=myfont3).place(x=20, y=243)
        kgf6 = Label(top,
                     text="Prabhas\n Rana Daggubati\n Tamannaah\n Anushka Shetty\n Ramya Krishna\n Sathyaraj\n Nassar",
                     font=myfont4).place(x=15, y=280)
        kgf7 = Label(top, text="Cast Crew:", font=myfont3).place(x=20, y=460)
        kgf_7 = Label(top,
                      text="Directed by  	S. S. Rajamouli \nProduced by  Shobu Yarlagadda \nWritten by  	K. V. Vijayendra Prasad\nScreenplay by  K. V. Vijayendra Prasad\nStory by K. V. Vijayendra Prasad",
                      font=myfont4).place(x=0, y=499)

        kgfr = Label(top, text="Select number of tickets:", font=("Verdana", 12)).place(x=700, y=120)
        ver = Scale(top, from_=0, to=20, orient=HORIZONTAL,command=seat_select).place(x=920, y=96)

        check = Checkbutton(top, text="Check this if you prefer corner seats").place(x=790, y=140)
        cineformat = Label(top, text="Cinema Class           :", font="Verdana").place(x=700, y=200)
        opt = ["Platinum (A - C) : 350 Rs. ", "Normal (D - F) : 175 Rs. ", "Budget (G - J) : 115 Rs. "]
        droptype = OptionMenu(top, var_3, *opt)
        var_3.set("Select")
        droptype.config(width=33, bg="#263D42", fg="white")
        droptype.place(x=920, y=200)
        click = Button(top, text="Click here for EXCITING COMBO OFFERS!!", font="verdana", bg="#263D42", fg="white",
                       width=42, height=3, command=_open2).place(x=810, y=250)
        click2 = Button(top, text="Or click here to proceed", font='arial', bg="#263D42", fg="white", width=42,
                        command=_topdestroy).place(x=810, y=335)
   if (var7.get()):
        kgf = Label(top, text="Baahubali 2: The Conclusion (U/A)", font=("Times 32", 47)).place(x=20, y=10)
        kgf1 = Label(top, text="(U/A)   .   2h 48m   .   Tamil   .   Action/Fantasy", font=myfont2).place(x=20, y=90)
        kgf3 = Label(top, text="Synopsis:", font=myfont3).place(x=20, y=120)
        kgf4 = Label(top,
                     text="After learning that his father was brutally killed \nby Bhallaladeva, Mahendra Baahubali raises an army to defeat him \nand release his mother from the former's captivity.",
                     font=myfont4).place(x=0, y=157)
        kgf5 = Label(top, text="Cast:", font=myfont3).place(x=20, y=243)
        kgf6 = Label(top, text="Prabhas\nRana Daggubati\nAnushka Shetty\nTamannaah\nRamya Krishna\nSathyaraj\nNassar",
                     font=myfont4).place(x=15, y=280)
        kgf7 = Label(top, text="Cast Crew:", font=myfont3).place(x=20, y=460)
        kgf_7 = Label(top,
                      text="Directed by  	S. S. Rajamouli \nProduced by  Shobu Yarlagadda \nWritten by K. V. Vijayendra Prasad\nScreenplay by  K. V. Vijayendra Prasad\nStory by K. V. Vijayendra Prasad",
                      font=myfont4).place(x=0, y=499)

        kgfr = Label(top, text="Select number of tickets:", font=("Verdana", 12)).place(x=700, y=120)
        ver = Scale(top, from_=0, to=20, orient=HORIZONTAL,command=seat_select).place(x=920, y=100)

        check = Checkbutton(top, text="Check this if you prefer corner seats").place(x=790, y=140)
        cineformat = Label(top, text="Cinema Class           :", font="Verdana").place(x=700, y=200)
        opt = ["Platinum (A - C) : 350 Rs. ", "Normal (D - F) : 175 Rs. ", "Budget (G - J) : 115 Rs. "]
        droptype = OptionMenu(top, var_3, *opt)
        var_3.set("Select")
        droptype.config(width=33, bg="#263D42", fg="white")
        droptype.place(x=920, y=200)
        click = Button(top, text="Click here for EXCITING COMBO OFFERS!!", font="verdana", bg="#263D42", fg="white",
                       width=42, height=3, command=_open2).place(x=810, y=250)
        click2 = Button(top, text="Or click here to proceed", font='arial', bg="#263D42", fg="white", width=42,
                        command=_topdestroy).place(x=810, y=335)
   if (var9.get()):
        kgf = Label(top, text="Petta (U/A)", font=("Times 32", 47)).place(x=20, y=10)
        kgf1 = Label(top, text="(U/A)   .   2h 52m   .   Tamil   .   Action/Drama", font=myfont2).place(x=20, y=90)
        kgf3 = Label(top, text="Synopsis:", font=myfont3).place(x=20, y=120)
        kgf4 = Label(top,
                     text="In a bid to save Anwar, his best friend's son, hostel\n warden Kaali, stands up against the local goons. However, \neverything goes haywire when Kaali is forced to face his past.",
                     font=myfont4).place(x=0, y=157)
        kgf5 = Label(top, text="Cast:", font=myfont3).place(x=20, y=243)
        kgf6 = Label(top,
                     text="Rajinikanth\nVijay Sethupathi\nSimran\nTrisha \n Sasikumar \nNawazuddin Siddiqui\nBobby Simha",
                     font=myfont4).place(x=15, y=280)
        kgf7 = Label(top, text="Cast Crew:", font=myfont3).place(x=20, y=460)
        kgf_7 = Label(top,
                      text="Directed by  Karthick Subbaraj \nProduced by  Kalanithi Maran \nWritten by Karthik Subbaraj \nScreenplay by  Karthik Subbaraj\nStory by Karthik Subbaraj",
                      font=myfont4).place(x=0, y=499)

        kgfr = Label(top, text="Select number of tickets:", font=("Verdana", 12)).place(x=700, y=120)
        ver = Scale(top, from_=0, to=20, orient=HORIZONTAL,command=seat_select).place(x=920, y=100)

        check = Checkbutton(top, text="Check this if you prefer corner seats").place(x=790, y=140)
        cineformat = Label(top, text="Cinema Class           :", font="Verdana").place(x=700, y=200)
        opt = ["Platinum (A - C) : 350 Rs. ", "Normal (D - F) : 175 Rs. ", "Budget (G - J) : 115 Rs. "]
        droptype = OptionMenu(top, var_3, *opt)
        var_3.set("Select")
        droptype.config(width=33, bg="#263D42", fg="white")
        droptype.place(x=920, y=200)
        click = Button(top, text="Click here for EXCITING COMBO OFFERS!!", font="verdana", bg="#263D42", fg="white",
                       width=42, height=3, command=_open2).place(x=810, y=250)
        click2 = Button(top, text="Or click here to proceed", font='arial', bg="#263D42", fg="white", width=42,
                        command=_topdestroy).place(x=810, y=335)
   if (var8.get()):
        kgf = Label(top, text="Bigil (U)", font=("Times 32", 47)).place(x=20, y=10)
        kgf1 = Label(top, text="(U)   .   2h 59m   .   Tamil   .   Action/Sport", font=myfont2).place(x=20, y=90)
        kgf3 = Label(top, text="Synopsis:", font=myfont3).place(x=20, y=120)
        kgf4 = Label(top,
                     text="Michael, an aggressive young man, gives up his dream of becoming a \nfootballer after his father's murder. However,a friend convinces him \nto coach a women's football team and turn his life around.",
                     font=myfont4).place(x=0, y=157)
        kgf5 = Label(top, text="Cast:", font=myfont3).place(x=20, y=243)
        kgf6 = Label(top, text="Vijay\nNayanthara\nJackie Shroff\nKathir\nVivek", font=myfont4).place(x=15, y=280)
        kgf7 = Label(top, text="Cast Crew:", font=myfont3).place(x=20, y=460)
        kgf_7 = Label(top,
                      text="Directed by  	Atlee \nProduced by  Kalpathi S. Aghoram \nWritten by  	Atlee\nScreenplay by  Atlee\nStory by Atlee",
                      font=myfont4).place(x=0, y=499)

        kgfr = Label(top, text="Select number of tickets:", font=("Verdana", 12)).place(x=700, y=120)
        ver = Scale(top, from_=0, to=20, orient=HORIZONTAL,command=seat_select).place(x=920, y=100)

        check = Checkbutton(top, text="Check this if you prefer corner seats").place(x=790, y=140)
        cineformat = Label(top, text="Cinema Class           :", font="Verdana").place(x=700, y=200)
        opt = ["Platinum (A - C) : 350 Rs. ", "Normal (D - F) : 175 Rs. ", "Budget (G - J) : 115 Rs. "]
        droptype = OptionMenu(top, var_3, *opt)
        var_3.set("Select")
        droptype.config(width=33, bg="#263D42", fg="white")
        droptype.place(x=920, y=200)
        click = Button(top, text="Click here for EXCITING COMBO OFFERS!!", font="verdana", bg="#263D42", fg="white",
                       width=42, height=3, command=_open2).place(x=810, y=250)
        click2 = Button(top, text="Or click here to proceed", font='arial', bg="#263D42", fg="white", width=42,
                        command=_topdestroy).place(x=810, y=335)
   if (var10.get()):
        kgf = Label(top, text="Joker (A)", font=("Times 32", 47)).place(x=20, y=10)
        kgf1 = Label(top, text="(A)   .   2h 2m   .   English   .   Drama/Crime", font=myfont2).place(x=20, y=90)
        kgf3 = Label(top, text="Synopsis:", font=myfont3).place(x=20, y=120)
        kgf4 = Label(top,
                     text="Arthur Fleck, a party clown, leads an impoverished life with his ailing\n mother. However, when society shuns him and brands him as a freak,\n he decides to embrace the life of crime and chaos.",
                     font=myfont4).place(x=0, y=157)
        kgf5 = Label(top, text="Cast:", font=myfont3).place(x=20, y=243)
        kgf6 = Label(top, text="Joaquin Phoenix\nRobert De Niro\nZazie Beetz\nFrances Conroy", font=myfont4).place(x=15,
                                                                                                                   y=280)
        kgf7 = Label(top, text="Cast Crew:", font=myfont3).place(x=20, y=460)
        kgf_7 = Label(top,
                      text="Directed by  	Todd Philips \nProduced by Bradley Cooper \nWritten by Todd Philips\nScreenplay by  Todd Philps\nStory by D.C Comics",
                      font=myfont4).place(x=0, y=499)

        kgfr = Label(top, text="Select number of tickets:", font=("Verdana", 12)).place(x=700, y=120)
        ver = Scale(top, from_=0, to=20, orient=HORIZONTAL,command=seat_select).place(x=920, y=100)

        check = Checkbutton(top, text="Check this if you prefer corner seats").place(x=790, y=140)
        cineformat = Label(top, text="Cinema Class           :", font="Verdana").place(x=700, y=200)
        opt = ["Platinum (A - C) : 350 Rs. ", "Normal (D - F) : 175 Rs. ", "Budget (G - J) : 115 Rs. "]
        droptype = OptionMenu(top, var_3, *opt)
        var_3.set("Select")
        droptype.config(width=33, bg="#263D42", fg="white")
        droptype.place(x=920, y=200)
        click = Button(top, text="Click here for EXCITING COMBO OFFERS!!", font="verdana", bg="#263D42", fg="white",
                       width=42, height=3, command=_open2).place(x=810, y=250)
        click2 = Button(top, text="Or click here to proceed", font='arial', bg="#263D42", fg="white", width=42,
                        command=_topdestroy).place(x=810, y=335)
        joker1=Label(top,text="Info:",font=abb,fg="red").place(x=700,y=400)
        joker2=Label(top,text="This movie has been rated 'A' and is for audience above the aga of 18.\nPlease carry a valid photo ID/age proof to the theatre. No refund of\ntickets once bought.",font=ab_,fg="red").place(x=700,y=435)
   if (var11.get()):
        kgf = Label(top, text="Inception (U/A)", font=("Times 32", 47)).place(x=20, y=10)
        kgf1 = Label(top, text="(U/A)   .   2h 42m   .   English   .   Action/Sci-fi", font=myfont2).place(x=20, y=90)
        kgf3 = Label(top, text="Synopsis:", font=myfont3).place(x=20, y=120)
        kgf4 = Label(top,
                     text="Cobb steals information from his targets by entering their dreams. Saito\noffers to wipe clean Cobb's criminal history as payment for performing an\n inception on his sick competitor's son.",
                     font=myfont4).place(x=0, y=157)
        kgf5 = Label(top, text="Cast:", font=myfont3).place(x=20, y=243)
        kgf6 = Label(top,
                     text="Leonardo DiCaprio\nKen Watanabe\nJoseph Gordon-Levitt\nMarion Cotillard\nEllen Page\nTom Hardy",
                     font=myfont4).place(x=15, y=280)
        kgf7 = Label(top, text="Cast Crew:", font=myfont3).place(x=20, y=460)
        kgf_7 = Label(top,
                      text="Directed by  	Cristopher Nolan \nProduced by Emma Thomas \nWritten by Christopher Nolan\nScreenplay by  Christopher Nolan",
                      font=myfont4).place(x=0, y=499)

        kgfr = Label(top, text="Select number of tickets:", font=("Verdana", 12)).place(x=700, y=120)
        ver = Scale(top, from_=0, to=20, orient=HORIZONTAL,command=seat_select).place(x=920, y=100)

        check = Checkbutton(top, text="Check this if you prefer corner seats").place(x=790, y=140)
        cineformat = Label(top, text="Cinema Class           :", font="Verdana").place(x=700, y=200)
        opt = ["Platinum (A - C) : 350 Rs. ", "Normal (D - F) : 175 Rs. ", "Budget (G - J) : 115 Rs. "]
        droptype = OptionMenu(top, var_3, *opt)
        var_3.set("Select")
        droptype.config(width=33, bg="#263D42", fg="white")
        droptype.place(x=920, y=200)
        click = Button(top, text="Click here for EXCITING COMBO OFFERS!!", font="verdana", bg="#263D42", fg="white",
                       width=42, height=3, command=_open2).place(x=810, y=250)
        click2 = Button(top, text="Or click here to proceed", font='arial', bg="#263D42", fg="white", width=42,
                        command=_topdestroy).place(x=810, y=335)
   if (var12.get()):
        kgf = Label(top, text="Tag (A)", font=("Times 32", 47)).place(x=20, y=10)
        kgf1 = Label(top, text="(A)   .   1h 45m   .   English   .   Comedy", font=myfont2).place(x=20, y=90)
        kgf3 = Label(top, text="Synopsis:", font=myfont3).place(x=20, y=120)
        kgf4 = Label(top,
                     text="A group of five friends, who have been playing the game of tag for 30 years,\n decide to play one last game before the wedding of their \nundefeated player.",
                     font=myfont4).place(x=0, y=157)
        kgf5 = Label(top, text="Cast:", font=myfont3).place(x=20, y=243)
        kgf6 = Label(top, text="Ed Helms\nJake Johnson\nAnnabelle Wallis\nHannibal Buress\nIsla Fisher",
                     font=myfont4).place(x=15, y=280)
        kgf7 = Label(top, text="Cast Crew:", font=myfont3).place(x=20, y=460)
        kgf_7 = Label(top,
                      text="Directed by  	Jeff Tomsic \nProduced by Todd Gamer \nWritten by Mark Steilen\nScreenplay by  Rob",
                      font=myfont4).place(x=0, y=499)

        kgfr = Label(top, text="Select number of tickets:", font=("Verdana", 12)).place(x=700, y=120)
        ver = Scale(top, from_=0, to=20, orient=HORIZONTAL,command=seat_select).place(x=920, y=100)

        check = Checkbutton(top, text="Check this if you prefer corner seats").place(x=790, y=140)
        cineformat = Label(top, text="Cinema Class           :", font="Verdana").place(x=700, y=200)
        opt = ["Platinum (A - C) : 350 Rs. ", "Normal (D - F) : 175 Rs. ", "Budget (G - J) : 115 Rs. "]
        droptype = OptionMenu(top, var_3, *opt)
        var_3.set("Select")
        droptype.config(width=33, bg="#263D42", fg="white")
        droptype.place(x=920, y=200)
        click = Button(top, text="Click here for EXCITING COMBO OFFERS!!", font="verdana", bg="#263D42", fg="white",
                       width=42, height=3, command=_open2).place(x=810, y=250)
        click2 = Button(top, text="Or click here to proceed", font='arial', bg="#263D42", fg="white", width=42,
                        command=_topdestroy).place(x=810, y=335)
        joker1=Label(top,text="Info:",font=abb,fg="red").place(x=700,y=400)
        joker2=Label(top,text="This movie has been rated 'A' and is for audience above the aga of 18.\nPlease carry a valid photo ID/age proof to the theatre. No refund of\ntickets once bought.",font=ab_,fg="red").place(x=700,y=435)
   if (var13.get()):
        kgf = Label(top, text="Indiana Jones (U/A)", font=("Times 32", 47)).place(x=20, y=10)
        kgf1 = Label(top, text="(U/A)   .   1h 55m   .   English   .   Adventure/Thriller", font=myfont2).place(x=20,
                                                                                                                y=90)
        kgf3 = Label(top, text="Synopsis:", font=myfont3).place(x=20, y=120)
        kgf4 = Label(top,
                     text="Archaeology professor Indiana Jones ventures to seize a biblical artefact known \nas the Ark of the Covenant. While doing so, he puts up a\n fight against Renee and a troop of Nazis.",
                     font=myfont4).place(x=0, y=157)
        kgf5 = Label(top, text="Cast:", font=myfont3).place(x=20, y=243)
        kgf6 = Label(top, text="Harrison Ford\nKaren Allen\nPaul Freeman\nRonald Lacey", font=myfont4).place(x=15,
                                                                                                             y=280)
        kgf7 = Label(top, text="Cast Crew:", font=myfont3).place(x=20, y=460)
        kgf_7 = Label(top,
                      text="Directed by  	Steven Spielberg\nProduced by Frank Marshall \nWritten by George Lucas\nScreenplay by  	Lawrence Kasdan",
                      font=myfont4).place(x=0, y=499)

        kgfr = Label(top, text="Select number of tickets:", font=("Verdana", 12)).place(x=700, y=120)
        ver = Scale(top, from_=0, to=20, orient=HORIZONTAL,command=seat_select).place(x=920, y=100)

        check = Checkbutton(top, text="Check this if you prefer corner seats").place(x=790, y=140)
        cineformat = Label(top, text="Cinema Class           :", font="Verdana").place(x=700, y=200)
        opt = ["Platinum (A - C) : 350 Rs. ", "Normal (D - F) : 175 Rs. ", "Budget (G - J) : 115 Rs. "]
        droptype = OptionMenu(top, var_3, *opt)
        var_3.set("Select")
        droptype.config(width=33, bg="#263D42", fg="white")
        droptype.place(x=920, y=200)
        click = Button(top, text="Click here for EXCITING COMBO OFFERS!!", font="verdana", bg="#263D42", fg="white",
                       width=42, height=3, command=_open2).place(x=810, y=250)
        click2 = Button(top, text="Or click here to proceed", font='arial', bg="#263D42", fg="white", width=42,
                        command=_topdestroy).place(x=810, y=335)
   if (var14.get()):
        kgf = Label(top, text="Avatar [3D] (U/A)", font=("Times 32", 47)).place(x=20, y=10)
        kgf1 = Label(top, text="(U/A)   .   2h 42m   .   English   .   Sci-fi/Action", font=myfont2).place(x=20, y=90)
        kgf3 = Label(top, text="Synopsis:", font=myfont3).place(x=20, y=120)
        kgf4 = Label(top,
                     text="Jake, who is paraplegic, replaces his twin on the Na'vi inhabited \nPandora for a corporate mission. After the natives accept him as one of their\n own, he must decide where his loyalties lie.",
                     font=myfont4).place(x=0, y=157)
        kgf5 = Label(top, text="Cast:", font=myfont3).place(x=20, y=243)
        kgf6 = Label(top, text="Sam Worthington\nZoe Saldana\nStephen Lang\nMichelle Rodriguez", font=myfont4).place(
            x=15, y=280)
        kgf7 = Label(top, text="Cast Crew:", font=myfont3).place(x=20, y=460)
        kgf_7 = Label(top, text="Directed by James Cameron\nProduced by Jon \nWritten by James Cameron",
                      font=myfont4).place(x=0, y=499)

        kgfr = Label(top, text="Select number of tickets:", font=("Verdana", 12)).place(x=700, y=120)
        ver = Scale(top, from_=0, to=20, orient=HORIZONTAL,command=seat_select).place(x=920, y=100)

        check = Checkbutton(top, text="Check this if you prefer corner seats").place(x=790, y=140)
        cineformat = Label(top, text="Cinema Class           :", font="Verdana").place(x=700, y=200)
        opt = ["Platinum (A - C) : 350 Rs. ", "Normal (D - F) : 175 Rs. ", "Budget (G - J) : 115 Rs. "]
        droptype = OptionMenu(top, var_3, *opt)
        var_3.set("Select")
        droptype.config(width=33, bg="#263D42", fg="white")
        droptype.place(x=920, y=200)
        click = Button(top, text="Click here for EXCITING COMBO OFFERS!!", font="verdana", bg="#263D42", fg="white",
                       width=42, height=3, command=_open2).place(x=810, y=250)
        click2 = Button(top, text="Or click here to proceed", font='arial', bg="#263D42", fg="white", width=42,
                        command=_topdestroy).place(x=810, y=335)
        joker1=Label(top,text="Info:",font=abb,fg="blue").place(x=700,y=400)
        joker2=Label(top,text="3-D glasses will be provided in the theatre .\nKindly return it after the movie ends.",font=ab_,fg="blue").place(x=700,y=435)
   if (var15.get()):
        kgf = Label(top, text="Athiran (PG-13)", font=("Times 32", 47)).place(x=20, y=10)
        kgf1 = Label(top, text="(PG-13)   .   2h 15m   .   Malayalam   .   Thriller/Horror", font=myfont2).place(x=20,
                                                                                                                 y=90)
        kgf3 = Label(top, text="Synopsis:", font=myfont3).place(x=20, y=120)
        kgf4 = Label(top,
                     text="Dr Nair, a psychiatrist, visits a mental asylum located in a remote\nlocation in Kerala. He meets a patient, Nithya, who is kept in isolation,\n and soon uncovers mysteries from her past.",
                     font=myfont4).place(x=0, y=157)
        kgf5 = Label(top, text="Cast:", font=myfont3).place(x=20, y=243)
        kgf6 = Label(top, text="Fahadh Faasil\nSai Pallavi\nAtul Kulkarni\nLena ", font=myfont4).place(x=15, y=280)
        kgf7 = Label(top, text="Cast Crew:", font=myfont3).place(x=20, y=460)
        kgf_7 = Label(top, text="Directed by Vivek\nProduced by Raju Mathew \nWritten by P.F.Matthews",
                      font=myfont4).place(x=0, y=499)

        kgfr = Label(top, text="Select number of tickets:", font=("Verdana", 12)).place(x=700, y=120)
        ver = Scale(top, from_=0, to=20, orient=HORIZONTAL,command=seat_select).place(x=920, y=100)

        check = Checkbutton(top, text="Check this if you prefer corner seats").place(x=790, y=140)
        cineformat = Label(top, text="Cinema Class           :", font="Verdana").place(x=700, y=200)
        opt = ["Platinum (A - C) : 350 Rs. ", "Normal (D - F) : 175 Rs. ", "Budget (G - J) : 115 Rs. "]
        droptype = OptionMenu(top, var_3, *opt)
        var_3.set("Select")
        droptype.config(width=33, bg="#263D42", fg="white")
        droptype.place(x=920, y=200)
        click = Button(top, text="Click here for EXCITING COMBO OFFERS!!", font="verdana", bg="#263D42", fg="white",
                       width=42, height=3, command=_open2).place(x=810, y=250)
        click2 = Button(top, text="Or click here to proceed", font='arial', bg="#263D42", fg="white", width=42,
                        command=_topdestroy).place(x=810, y=335)
   if (var16.get()):
        kgf = Label(top, text="Kireedam (U)", font=("Times 32", 47)).place(x=20, y=10)
        kgf1 = Label(top, text="(U)   .   2h 20m   .   Malayalam   .   Drama/Action", font=myfont2).place(x=20, y=90)
        kgf3 = Label(top, text="Synopsis:", font=myfont3).place(x=20, y=120)
        kgf4 = Label(top,
                     text="Sethu aspires to become a police officer to fulfil his father's dream.\n However, his life turns upside down when he intervenes in a scuffle with\na criminal to save his father's life.",
                     font=myfont4).place(x=0, y=157)
        kgf5 = Label(top, text="Cast:", font=myfont3).place(x=20, y=243)
        kgf6 = Label(top, text="Mohanlal\nThilakan\nParvathy Jayaram\nMohan Raj ", font=myfont4).place(x=15, y=280)
        kgf7 = Label(top, text="Cast Crew:", font=myfont3).place(x=20, y=460)
        kgf_7 = Label(top, text="Directed by Sibi Malayil\nProduced by Dinesh Panicker \nWritten by A.K.Lohithadas",
                      font=myfont4).place(x=0, y=499)

        kgfr = Label(top, text="Select number of tickets:", font=("Verdana", 12)).place(x=700, y=120)
        ver = Scale(top, from_=0, to=20, orient=HORIZONTAL,command=seat_select).place(x=920, y=100)

        check = Checkbutton(top, text="Check this if you prefer corner seats").place(x=790, y=140)
        cineformat = Label(top, text="Cinema Class           :", font="Verdana").place(x=700, y=200)
        opt = ["Platinum (A - C) : 350 Rs. ", "Normal (D - F) : 175 Rs. ", "Budget (G - J) : 115 Rs. "]
        droptype = OptionMenu(top, var_3, *opt)
        var_3.set("Select")
        droptype.config(width=33, bg="#263D42", fg="white")
        droptype.place(x=920, y=200)
        click = Button(top, text="Click here for EXCITING COMBO OFFERS!!", font="verdana", bg="#263D42", fg="white",
                       width=42, height=3, command=_open2).place(x=810, y=250)
        click2 = Button(top, text="Or click here to proceed", font='arial', bg="#263D42", fg="white", width=42,
                        command=_topdestroy).place(x=810, y=335)
   if (var17.get()):
        kgf = Label(top, text="Mathilukal (U)", font=("Times 32", 47)).place(x=20, y=10)
        kgf1 = Label(top, text="(U)   .   2h    .   Malayalam   .   Drama/Romance", font=myfont2).place(x=20, y=90)
        kgf3 = Label(top, text="Synopsis:", font=myfont3).place(x=20, y=120)
        kgf4 = Label(top,
                     text="Bashir, who has been imprisoned, falls in love with his inmate, Narayani. \nWith the wall keeping them apart, will Bashir win her heart?",
                     font=myfont4).place(x=0, y=157)
        kgf5 = Label(top, text="Cast:", font=myfont3).place(x=20, y=243)
        kgf6 = Label(top, text="Mammootty\n Murali\n Ravi \nThilakan\n K.P.A.C.Lalitha\n Babu", font=myfont4).place(
            x=15, y=280)
        kgf7 = Label(top, text="Cast Crew:", font=myfont3).place(x=20, y=460)
        kgf_7 = Label(top,
                      text="Directed by Adoor Gopalakrishan\nProduced by Adoor Gopalakrishnan \nWritten by Adoor Gopalakrishnan\n Screenplay by Basheer",
                      font=myfont4).place(x=0, y=499)

        kgfr = Label(top, text="Select number of tickets:", font=("Verdana", 12)).place(x=700, y=120)
        ver = Scale(top, from_=0, to=20, orient=HORIZONTAL,command=seat_select).place(x=920, y=100)

        check = Checkbutton(top, text="Check this if you prefer corner seats").place(x=790, y=140)
        cineformat = Label(top, text="Cinema Class           :", font="Verdana").place(x=700, y=200)
        opt = ["Platinum (A - C) : 350 Rs. ", "Normal (D - F) : 175 Rs. ", "Budget (G - J) : 115 Rs. "]
        droptype = OptionMenu(top, var_3, *opt)
        var_3.set("Select")
        droptype.config(width=33, bg="#263D42", fg="white")
        droptype.place(x=920, y=200)
        click = Button(top, text="Click here for EXCITING COMBO OFFERS!!", font="verdana", bg="#263D42", fg="white",
                       width=42, height=3, command=_open2).place(x=810, y=250)
        click2 = Button(top, text="Or click here to proceed", font='arial', bg="#263D42", fg="white", width=42,
                        command=_topdestroy).place(x=810, y=335)
   if (var18.get()):
        kgf = Label(top, text="Helen (U/A)", font=("Times 32", 47)).place(x=20, y=10)
        kgf1 = Label(top, text="(U/A)   .   1h 57m   .   Malayalam   .   Drama/Thriller", font=myfont2).place(x=20,
                                                                                                              y=90)
        kgf3 = Label(top, text="Synopsis:", font=myfont3).place(x=20, y=120)
        kgf4 = Label(top,
                     text="Helen, a young nurse, wishes to relocate to Canada. However, things take an\n ugly turn when she does not return home from work and suddenly\n disappears.",
                     font=myfont4).place(x=0, y=157)
        kgf5 = Label(top, text="Cast:", font=myfont3).place(x=20, y=243)
        kgf6 = Label(top, text="Anna Ben\nLal\nNoble Babu Thomas\nAju Varghese", font=myfont4).place(x=15, y=280)
        kgf7 = Label(top, text="Cast Crew:", font=myfont3).place(x=20, y=460)
        kgf_7 = Label(top,
                      text="Directed by Mathukutty Xavier\nProduced by Vineeth \nWritten by Mathukutty Xavier\n Screenplay by Alfred Kurian Joseph",
                      font=myfont4).place(x=0, y=499)

        kgfr = Label(top, text="Select number of tickets:", font=("Verdana", 12)).place(x=700, y=120)
        ver = Scale(top, from_=0, to=20, orient=HORIZONTAL,command=seat_select).place(x=920, y=100)

        check = Checkbutton(top, text="Check this if you prefer corner seats").place(x=790, y=140)
        cineformat = Label(top, text="Cinema Class           :", font="Verdana").place(x=700, y=200)
        opt = ["Platinum (A - C) : 350 Rs. ", "Normal (D - F) : 175 Rs. ", "Budget (G - J) : 115 Rs. "]
        droptype = OptionMenu(top, var_3, *opt)
        var_3.set("Select")
        droptype.config(width=33, bg="#263D42", fg="white")
        droptype.place(x=920, y=200)
        click = Button(top, text="Click here for EXCITING COMBO OFFERS!!", font="verdana", bg="#263D42", fg="white",
                       width=42, height=3, command=_open2).place(x=810, y=250)
        click2 = Button(top, text="Or click here to proceed", font='arial', bg="#263D42", fg="white", width=42,
                        command=_topdestroy).place(x=810, y=335)
   if (var19.get()):
        kgf = Label(top, text="Thondimuthalum Driksakshiyum(U/A)", font=("Times 32", 47)).place(x=20, y=10)
        kgf1 = Label(top, text="(U/A)   .   2h 15m   .   Malayalam   .   Drama/Thriller", font=myfont2).place(x=20,
                                                                                                              y=90)
        kgf3 = Label(top, text="Synopsis:", font=myfont3).place(x=20, y=120)
        kgf4 = Label(top,
                     text="Newly-weds Sreeja and Prasad struggle to cope with their lives and decide \nto sell Sreeja's gold chain for money. However, a thief steals the\n chain during a bus journey, adding to their woes.",
                     font=myfont4).place(x=0, y=157)
        kgf5 = Label(top, text="Cast:", font=myfont3).place(x=20, y=243)
        kgf6 = Label(top, text="Suraj Venjaramoodu\nFahadh Faasil\nNimisha Sajayan\nMini K. S\nAlencier Ley Lopez",
                     font=myfont4).place(x=15, y=280)
        kgf7 = Label(top, text="Cast Crew:", font=myfont3).place(x=20, y=460)
        kgf_7 = Label(top,
                      text="Directed by Dileesh Pothan\nProduced by Sandip Senan\nWritten by Sajeev Pazhoor\n Screenplay by Dileesh Pothan",
                      font=myfont4).place(x=0, y=499)

        kgfr = Label(top, text="Select number of tickets:", font=("Verdana", 12)).place(x=700, y=120)
        ver = Scale(top, from_=0, to=20, orient=HORIZONTAL,command=seat_select).place(x=920, y=100)

        check = Checkbutton(top, text="Check this if you prefer corner seats").place(x=790, y=140)
        cineformat = Label(top, text="Cinema Class           :", font="Verdana").place(x=700, y=200)
        opt = ["Platinum (A - C) : 350 Rs. ", "Normal (D - F) : 175 Rs. ", "Budget (G - J) : 115 Rs. "]
        droptype = OptionMenu(top, var_3, *opt)
        var_3.set("Select")
        droptype.config(width=33, bg="#263D42", fg="white")
        droptype.place(x=920, y=200)
        click = Button(top, text="Click here for EXCITING COMBO OFFERS!!", font="verdana", bg="#263D42", fg="white",
                       width=42, height=3, command=_open2).place(x=810, y=250)
        click2 = Button(top, text="Or click here to proceed", font='arial', bg="#263D42", fg="white", width=42,
                        command=_topdestroy).place(x=810, y=335)
   top.mainloop()



def com():
    m = Label(root, text=combo.get()).pack()


def _1to2():
    global frame2, c1, dat, var3, var4
    print(var3.get())
    frame1.pack_forget()

    if var2.get() == 'Tamil':
        label_2 = Label(root, text="NOW SHOWING", font=("Times 32", 47)).place(x=20, y=10)
        c1 = Checkbutton(root, text="K.G.F", font=("Verdana", 23), variable=var5).place(x=235, y=110)
        c2 = Checkbutton(root, text="Baahubali: The Beginning", font=("Verdana", 23), variable=var6).place(x=400, y=110)
        c3 = Checkbutton(root, text="Baahubali 2: The Conclusion", font=("Verdana", 23), variable=var7).place(x=850,
                                                                                                              y=110)
        c4 = Checkbutton(root, text="Bigil", font=("Verdana", 23), variable=var8).place(x=820, y=190)
        c5 = Checkbutton(root, text="Petta", font=("Verdana", 23), variable=var9).place(x=450, y=190)
        label_3 = Label(root, text="Your Safety is our Top Priority", font=myfont).place(x=120, y=350)
        label_4 = Label(root, text="Use of Masks is mandatory", font=myfont).place(x=165, y=390)
        label_5 = Label(root, text="Sanitization After Each Show", font=myfont).place(x=120, y=430)
        label_6 = Label(root, text="Social Distancing in Cinema Halls", font=myfont).place(x=165, y=470)
        var3 = StringVar()
        var4 = StringVar()
        options = ['1', '2', '3', '4', '5', '6', '7', '8', '9', '10', '11', '12', '13', '14', '15', '16', '17', '18',
                   '19', '20', '21', '22', '23', '24', '25', '26', '27', '28', '29', '30', '31']
        options1 = ['December,2020', 'January,2021']
        dropdate = OptionMenu(root, var3, *options)
        var3.set("Select Date")
        dropdate.config(width=10, bg="#263D42", fg="white")
        dat = var3.get()
        dropdate.place(x=900, y=350)
        dropmonth = OptionMenu(root, var4, *options1)
        var4.set("Select Month")
        dropmonth.config(width=13, bg="#263D42", fg="white")
        dropmonth.place(x=1010, y=350)

        btn1 = Button(root, text="Click here to proceed", width=25, bg="#263D42", fg="white", font="Times",
                      command=_open).place(x=903, y=417)


    if var2.get() == 'English':
        label_2 = Label(root, text="NOW SHOWING", font=("Times 32", 47)).place(x=20, y=10)
        c1 = Checkbutton(root, text="Joker", font=myfont1, variable=var10).place(x=235, y=110)
        c2 = Checkbutton(root, text="Inception", font=myfont1, variable=var11).place(x=500, y=110)
        c3 = Checkbutton(root, text="Tag", font=myfont1, variable=var12).place(x=850, y=110)
        c4 = Checkbutton(root, text="Indiana Jones", font=myfont1, variable=var13).place(x=760, y=190)
        c5 = Checkbutton(root, text="Avatar [3D]", font=myfont1, variable=var14).place(x=375, y=190)
        label_3 = Label(root, text="Your Safety is our Top Priority", font=myfont).place(x=120, y=350)
        label_4 = Label(root, text="Use of Masks is mandatory", font=myfont).place(x=165, y=390)
        label_5 = Label(root, text="Sanitization After Each Show", font=myfont).place(x=120, y=430)
        label_6 = Label(root, text="Social Distancing in Cinema Halls", font=myfont).place(x=165, y=470)
        var3 = StringVar()
        var4 = StringVar()
        options = ['1', '2', '3', '4', '5', '6', '7', '8', '9', '10', '11', '12', '13', '14', '15', '16', '17', '18',
                   '19', '20', '21', '22', '23', '24', '25', '26', '27', '28', '29', '30', '31']
        options1 = ['December,2020', 'January,2021']
        dropdate = OptionMenu(root, var3, *options)
        var3.set("Select Date")
        dropdate.config(width=10, bg="#263D42", fg="white")
        dropdate.place(x=900, y=350)
        dropmonth = OptionMenu(root, var4, *options1)
        var4.set("Select Month")
        dropmonth.config(width=13, bg="#263D42", fg="white")
        dropmonth.place(x=1010, y=350)
        btn2 = Button(root, text="Click here to proceed", width=25, bg="#263D42", fg="white", font="Times",
                      command=_open).place(x=903, y=417)
    if var2.get() == 'Malayalam':
        label_2 = Label(root, text="NOW SHOWING", font=("Times 32", 47)).place(x=20, y=10)
        c1 = Checkbutton(root, text="Athiran", font=myfont1, variable=var15).place(x=235, y=110)
        c2 = Checkbutton(root, text="Kireedam", font=myfont1, variable=var16).place(x=500, y=110)
        c3 = Checkbutton(root, text="Mathilukal", font=myfont1, variable=var17).place(x=850, y=110)
        c4 = Checkbutton(root, text="Helen", font=myfont1, variable=var18).place(x=360, y=190)
        c5 = Checkbutton(root, text="Thondimuthalum Driksakshiyum", font=myfont1, variable=var19).place(x=695, y=190)
        label_3 = Label(root, text="Your Safety is our Top Priority", font=myfont).place(x=120, y=350)
        label_4 = Label(root, text="Use of Masks is mandatory", font=myfont).place(x=165, y=390)
        label_5 = Label(root, text="Sanitization After Each Show", font=myfont).place(x=120, y=430)
        label_6 = Label(root, text="Social Distancing in Cinema Halls", font=myfont).place(x=165, y=470)
        var3 = StringVar()
        var4 = StringVar()
        options = ['1', '2', '3', '4', '5', '6', '7', '8', '9', '10', '11', '12', '13', '14', '15', '16', '17', '18',
                   '19', '20', '21', '22', '23', '24', '25', '26', '27', '28', '29', '30', '31']
        options1 = ['December,2020', 'January,2021']
        dropdate = OptionMenu(root, var3, *options)
        var3.set("Select Date")
        dropdate.config(width=10, bg="#263D42", fg="white")
        dropdate.place(x=900, y=350)
        dropmonth = OptionMenu(root, var4, *options1)
        var4.set("Select Month")
        dropmonth.config(width=13, bg="#263D42", fg="white")
        dropmonth.place(x=1010, y=350)
        btn3 = Button(root, text="Click here to proceed", width=25, bg="#263D42", fg="white", font="Times",
                      command=_open).place(x=903, y=417)
    frame2.pack()
frame1 = Frame(root)
frame2 = Frame(root)
frame3 = Frame(root)

def _frame1():
    label1 = Label(frame1, text="Welcome to CineMagic!", font="Times 32", width=100, anchor=W).pack()
    label5 = Label(frame1, text="Online Movie tickets Booking for theatre chains in Coimbatore", font="Times 32",
                   width=100, height=2, anchor=NE).pack()
    list1 = ['K.G BIG CINEMAS A/C DTS', 'Carnatic A/c 3-D', 'Archana & Darsana Theatres', 'INOX(Prozone)',
             'The Cinema(BrookFields)']
    list2 = ['Tamil', 'English', 'Malayalam']
    droplist = OptionMenu(frame1, var, *list1)
    var.set("Select Theatre")
    droplist.config(width=30, bg="#263D42", fg="white")
    droplist.place(x=500, y=130)
    dlist = OptionMenu(frame1, var2, *list2)
    var2.set("Language")
    dlist.config(width=20, bg="#263D42", fg="white")
    dlist.place(x=350, y=130)
    b1 = Button(frame1, text="Click to Proceed", width=30, bg="#263D42", fg="white", command=_1to2).place(x=723, y=133)
    frame1.pack()


_frame1()
root.mainloop()
