# PythonProject
#face-recognaition-syatem.

#main.py
from tkinter import*
from tkinter import ttk
from PIL import Image, ImageTk
from Student import Student


class Face_Recognition_System:
    def __init__(self, root):
        self.root = root
        self.root.geometry("1530x790+0+0")
        self.root.title("Face Recognition System")

    

        # First image
        img=Image.open(r"C:\Users\mahiv\OneDrive\Pictures\ALLpHOTO\download (1).jpeg")
        img=img.resize((500,130),Image.Resampling.LANCZOS)
        self.Photoimg=ImageTk.PhotoImage(img)

        f_lbl=Label(self.root,image=self.Photoimg)
        f_lbl.place(x=0,y=0,width=490,height=128)

        #seond img
        img1=Image.open(r"C:\Users\mahiv\OneDrive\Pictures\ALLpHOTO\download.jpeg")
        img1=img1.resize((500,130),Image.Resampling.LANCZOS)
        self.Photoimg1=ImageTk.PhotoImage(img1)

        f_lbl=Label(self.root,image=self.Photoimg1)
        f_lbl.place(x=500,y=0,width=500,height=130)
         
        #Third img
        img2=Image.open(r"C:\Users\mahiv\OneDrive\Pictures\ALLpHOTO\download (2).jpeg")
        img2=img2.resize((500,130),Image.Resampling.LANCZOS)
        self.Photoimg2=ImageTk.PhotoImage(img2)

        f_lbl=Label(self.root,image=self.Photoimg2)
        f_lbl.place(x=1000,y=0,width=550,height=130)
        
        #bg img

        img3=Image.open(r"C:\Users\mahiv\OneDrive\Pictures\ALLpHOTO\bgPhoto.jpg")
        img3=img3.resize((1530,710),Image.Resampling.LANCZOS)
        self.Photoimg3=ImageTk.PhotoImage(img3)

        bg_img=Label(self.root,image=self.Photoimg3)
        bg_img.place(x=0,y=130,width=1530,height=710)

        #titel

        title=Label(bg_img,text="FACE RECOGNAITION SYSTEM SOFTWARE",font=("times new roman",35,"bold"),bg="white",fg="red")
        title.place(x=0,y=0,width=1530,height=45)

        # student button
        img4=Image.open(r"C:\Users\mahiv\OneDrive\Pictures\ALLpHOTO\download (3).jpeg")
        img4=img4.resize((220,220),Image.Resampling.LANCZOS)
        self.Photoimg4=ImageTk.PhotoImage(img4)

        b1=Button(bg_img,command=self.student_details,image=self.Photoimg4,cursor="hand2")
        b1.place(x=200,y=100,width=220,height=220)

        b1_1=Button(bg_img,command=self.student_details,text="Student details",cursor="hand2",font=("times new roman",15,"bold"),bg="blue",fg="white")
        b1_1.place(x=200,y=300,width=220,height=40)

        #Detect face button

        img5=Image.open(r"C:\Users\mahiv\OneDrive\Pictures\ALLpHOTO\detect.jpeg")
        img5=img5.resize((220,220),Image.Resampling.LANCZOS)
        self.Photoimg5=ImageTk.PhotoImage(img5)

        b1=Button(bg_img,image=self.Photoimg5,cursor="hand2")
        b1.place(x=500,y=100,width=220,height=220)

        b1_1=Button(bg_img,text="Face Detector",cursor="hand2",font=("times new roman",15,"bold"),bg="blue",fg="white")
        b1_1.place(x=500,y=300,width=220,height=40)

        # Attendance face button 

        img6=Image.open(r"C:\Users\mahiv\OneDrive\Pictures\ALLpHOTO\attendance.jpeg")
        img6=img6.resize((220,220),Image.Resampling.LANCZOS)
        self.Photoimg6=ImageTk.PhotoImage(img6)

        b1=Button(bg_img,image=self.Photoimg6,cursor="hand2")
        b1.place(x=800,y=100,width=220,height=220)

        b1_1=Button(bg_img,text="Attendance",cursor="hand2",font=("times new roman",15,"bold"),bg="blue",fg="white")
        b1_1.place(x=800,y=300,width=220,height=40)

       # Help face button
        img7=Image.open(r"C:\Users\mahiv\OneDrive\Pictures\ALLpHOTO\help.jpeg")
        img7=img7.resize((220,220),Image.Resampling.LANCZOS)
        self.Photoimg7=ImageTk.PhotoImage(img7)

        b1=Button(bg_img,image=self.Photoimg7,cursor="hand2")
        b1.place(x=1100,y=100,width=220,height=220)

        b1_1=Button(bg_img,text="Help desk",cursor="hand2",font=("times new roman",15,"bold"),bg="blue",fg="white")
        b1_1.place(x=1100,y=300,width=220,height=40)

         # Train face button

        img8=Image.open(r"C:\Users\mahiv\OneDrive\Pictures\ALLpHOTO\train.jpg")
        img8=img8.resize((220,220),Image.Resampling.LANCZOS)
        self.Photoimg8=ImageTk.PhotoImage(img8)

        b1=Button(bg_img,image=self.Photoimg8,cursor="hand2")
        b1.place(x=200,y=380,width=220,height=220)

        b1_1=Button(bg_img,text="Train Data",cursor="hand2",font=("times new roman",15,"bold"),bg="blue",fg="white")
        b1_1.place(x=200,y=580,width=220,height=40)
       

        #Photo face
        img9=Image.open(r"C:\Users\mahiv\OneDrive\Pictures\ALLpHOTO\photos.jpeg")
        img9=img9.resize((220,220),Image.Resampling.LANCZOS)
        self.Photoimg9=ImageTk.PhotoImage(img9)

        b1=Button(bg_img,image=self.Photoimg9,cursor="hand2")
        b1.place(x=500,y=380,width=220,height=220)

        b1_1=Button(bg_img,text="Photos",cursor="hand2",font=("times new roman",15,"bold"),bg="blue",fg="white")
        b1_1.place(x=500,y=580,width=220,height=40)

        #Developers

        img10=Image.open(r"C:\Users\mahiv\OneDrive\Pictures\ALLpHOTO\developer.jpeg")
        img8=img10.resize((220,220),Image.Resampling.LANCZOS)
        self.Photoimg10=ImageTk.PhotoImage(img10)

        b1=Button(bg_img,image=self.Photoimg10,cursor="hand2")
        b1.place(x=800,y=380,width=220,height=220)

        b1_1=Button(bg_img,text="Developer",cursor="hand2",font=("times new roman",15,"bold"),bg="blue",fg="white")
        b1_1.place(x=800,y=580,width=220,height=40)

        # Exit face button

        img11=Image.open(r"C:\Users\mahiv\OneDrive\Pictures\ALLpHOTO\EXIT.jpeg")
        img11=img11.resize((220,220),Image.Resampling.LANCZOS)
        self.Photoimg11=ImageTk.PhotoImage(img11)

        b1=Button(bg_img,image=self.Photoimg11,cursor="hand2")
        b1.place(x=1100,y=380,width=220,height=220)

        b1_1=Button(bg_img,text="Exite",cursor="hand2",font=("times new roman",15,"bold"),bg="blue",fg="white")
        b1_1.place(x=1100,y=580,width=220,height=40)
    

       #=======function detials==========

    def student_details(self):
            print("Student details button clicked")
            self.new_window=Toplevel(self.root)
            self.app=Student(self.new_window)
            
            
            


        

        


if __name__ == "__main__":
    root = Tk()
    obj = Face_Recognition_System(root)
    root.mainloop()
