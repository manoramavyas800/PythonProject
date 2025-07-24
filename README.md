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

    #student.py
    from tkinter import*
from tkinter import ttk
from PIL import Image, ImageTk
from tkinter import messagebox


class Student:
    def __init__(self, root):
        self.root = root
        self.root.geometry("1530x790+0+0")
        self.root.title("Face Recognition System")


        # ============varible =========
        self.var_dep=StringVar()
        self.var_course=StringVar()
        self.var_year=StringVar()
        self.var_sem=StringVar()
        self.var_id=StringVar()
        self.var_name=StringVar()
        self.var_div=StringVar()
        self.var_rollno=StringVar()
        self.var_gender=StringVar()
        self.var_dob=StringVar()
        self.var_email=StringVar()
        self.var_phone=StringVar()
        self.var_add=StringVar()
        self.var_teacher=StringVar()

         # First image
        img=Image.open(r"C:\Users\mahiv\OneDrive\Pictures\ALLpHOTO\STU1.jpeg")
        img=img.resize((500,130),Image.Resampling.LANCZOS)
        self.Photoimg=ImageTk.PhotoImage(img)

        f_lbl=Label(self.root,image=self.Photoimg)
        f_lbl.place(x=0,y=0,width=490,height=128)

        #seond img
        img1=Image.open(r"C:\Users\mahiv\OneDrive\Pictures\ALLpHOTO\STU2.jpeg")
        img1=img1.resize((500,130),Image.Resampling.LANCZOS)
        self.Photoimg1=ImageTk.PhotoImage(img1)

        f_lbl=Label(self.root,image=self.Photoimg1)
        f_lbl.place(x=500,y=0,width=500,height=130)
         
        #Third img
        img2=Image.open(r"C:\Users\mahiv\OneDrive\Pictures\ALLpHOTO\STU3.jpeg")
        img2=img2.resize((500,130),Image.Resampling.LANCZOS)
        self.Photoimg2=ImageTk.PhotoImage(img2)

        f_lbl=Label(self.root,image=self.Photoimg2)
        f_lbl.place(x=1000,y=0,width=550,height=130)
        
        #bg img

        img3=Image.open(r"C:\Users\mahiv\OneDrive\Pictures\ALLpHOTO\BG2.jpeg")
        img3=img3.resize((1530,710),Image.Resampling.LANCZOS)
        self.Photoimg3=ImageTk.PhotoImage(img3)

        bg_img=Label(self.root,image=self.Photoimg3)
        bg_img.place(x=0,y=130,width=1530,height=710)

        #titel

        title=Label(bg_img,text="STUDENT MANAGMENT ",font=("times new roman",35,"bold"),bg="white",fg="red")
        title.place(x=0,y=0,width=1530,height=45)

        main_fream=Frame(bg_img,bd=2,bg="white")
        main_fream.place(x=20,y=55,width=1480,height=600)


        #left lable

        left_fream=LabelFrame(main_fream,bd=2,bg="white",relief=RIDGE,text="Student Details",font=("times new roman",12,"bold"))
        left_fream.place(x=10,y=10,width=730,height=580)

        img_left=Image.open(r"C:\Users\mahiv\OneDrive\Pictures\ALLpHOTO\left2.jpeg")
        img_left=img_left.resize((720,130),Image.Resampling.LANCZOS)
        self.Photoimg_left=ImageTk.PhotoImage(img_left)

        f_lbl=Label(left_fream,image=self.Photoimg_left)
        f_lbl.place(x=5,y=0,width=720,height=130)

        #current course

        current_course_frame=LabelFrame(left_fream,bd=2,bg="white",relief=RIDGE,text="Current Course",font=("times new roman",12,"bold"))
        current_course_frame.place(x=5,y=135,width=720,height=150)


        dep_lable=Label(current_course_frame,text="Department",font=("times new roman",12,"bold"),bg="white")
        dep_lable.grid(row=0,column=0,padx=10)

        dep_combo=ttk.Combobox(current_course_frame,font=("times new roman",12,"bold"),state="readonly")
        dep_combo["value"]=("Select Department","Computer","IT","Civil","Mechnical",)
        dep_combo.current(0)          
        dep_combo.grid(row=0, column=1,padx=2,pady=10)            

        # Department

        dep_lable1=Label(current_course_frame,text="Department",font=("times new roman",13,"bold"),bg="white")
        dep_lable1.grid(row=0,column=0,padx=10,sticky=W)

        dep_combo=ttk.Combobox(current_course_frame,textvariable=self.var_dep,font=("times new roman",13,"bold"),state="readonly",width=20)
        dep_combo["value"]=("Select Department","Computer","IT","Civil","Mechnical")
        dep_combo.current(0)          
        dep_combo.grid(row=0, column=1,padx=2,pady=10,sticky=W) 

        #Course

        course_lable1=Label(current_course_frame,text="Course",font=("times new roman",13,"bold"),bg="white")
        course_lable1.grid(row=0,column=2,padx=10,sticky=W)

        course_combo=ttk.Combobox(current_course_frame,textvariable=self.var_add,font=("times new roman",13,"bold"),state="readonly",width=20)
        course_combo["value"]=("Select Course","FE","SE","TE","BE")
        course_combo.current(0)          
        course_combo.grid(row=0, column=3,padx=2,pady=10,sticky=W) 

        #YEAR

        year_lable1=Label(current_course_frame,text="Year",font=("times new roman",13,"bold"),bg="white")
        year_lable1.grid(row=1,column=0,padx=10,sticky=W)

        year_combo=ttk.Combobox(current_course_frame,textvariable=self.var_year,font=("times new roman",13,"bold"),state="readonly",width=20)
        year_combo["value"]=("Select Year","2020-21","2021-22","2022-23","2023-24")
        year_combo.current(0)          
        year_combo.grid(row=1, column=1,padx=2,pady=10,sticky=W) 

        #Semester

        sem_lable1=Label(current_course_frame,text="Semester",font=("times new roman",13,"bold"),bg="white")
        sem_lable1.grid(row=1,column=2,padx=10,sticky=W)

        sem_combo=ttk.Combobox(current_course_frame,textvariable=self.var_sem,font=("times new roman",13,"bold"),state="readonly",width=20)
        sem_combo["value"]=("Select Semester","sem-1","sem-2","sem-3","sem-4")
        sem_combo.current(0)          
        sem_combo.grid(row=1, column=3,padx=2,pady=10,sticky=W)


        #Student

        student_frame=LabelFrame(left_fream,bd=2,bg="white",relief=RIDGE,text="Class Student Information",font=("times new roman",12,"bold"))
        student_frame.place(x=5,y=250,width=720,height=300)
        
        #Stusent id
        studentId_lable1=Label(student_frame,text="StudentID:",font=("times new roman",13,"bold"),bg="white")
        studentId_lable1.grid(row=0,column=0,padx=10,pady=5,sticky=W)

        studentID_entry=ttk.Entry(student_frame,textvariable=self.var_id,width=20,font=("times new roman",13,"bold"))
        studentID_entry.grid(row=0,column=1,padx=10,pady=5,sticky=W)

        #Stusent name
        studentName_lable1=Label(student_frame,text="Student Name:",font=("times new roman",13,"bold"),bg="white")
        studentName_lable1.grid(row=0,column=2,padx=10,pady=5,sticky=W)

        studentName_entry=ttk.Entry(student_frame,textvariable=self.var_name,width=20,font=("times new roman",13,"bold"))
        studentName_entry.grid(row=0,column=3,padx=10,pady=5,sticky=W)

        #class division
        class_lable1=Label(student_frame,text="Class Division:",font=("times new roman",13,"bold"),bg="white")
        class_lable1.grid(row=1,column=0,padx=10,pady=5,sticky=W)

        class_entry=ttk.Entry(student_frame,textvariable=self.var_dep,width=20,font=("times new roman",13,"bold"))
        class_entry.grid(row=1,column=1,padx=10,pady=5,sticky=W)
         
         # Roll no
        rollno_lable1=Label(student_frame,text="Roll NO:",font=("times new roman",13,"bold"),bg="white")
        rollno_lable1.grid(row=1,column=2,padx=10,pady=5,sticky=W)

        rollno_entry=ttk.Entry(student_frame,textvariable=self.var_rollno,width=20,font=("times new roman",13,"bold"))
        rollno_entry.grid(row=1,column=3,padx=10,pady=5,sticky=W)

       #Gender

        gen_lable1=Label(student_frame,text="Gender :",font=("times new roman",13,"bold"),bg="white")
        gen_lable1.grid(row=2,column=0,padx=10,pady=5,sticky=W)

        gen_entry=ttk.Entry(student_frame,textvariable=self.var_gender,width=20,font=("times new roman",13,"bold"))
        gen_entry.grid(row=2,column=1,padx=10,pady=5,sticky=W)

        #DOB

        dob_lable1=Label(student_frame,text="DOB :",font=("times new roman",13,"bold"),bg="white")
        dob_lable1.grid(row=2,column=2,padx=10,pady=5,sticky=W)

        dob_entry=ttk.Entry(student_frame,textvariable=self.var_dob,width=20,font=("times new roman",13,"bold"))
        dob_entry.grid(row=2,column=3,padx=10,pady=5,sticky=W)

        #Email

        email_lable1=Label(student_frame,text="Email:",font=("times new roman",13,"bold"),bg="white")
        email_lable1.grid(row=3,column=0,padx=10,pady=5,sticky=W)

        email_entry=ttk.Entry(student_frame,textvariable=self.var_email,width=20,font=("times new roman",13,"bold"))
        email_entry.grid(row=3,column=1,padx=10,pady=5,sticky=W)

        #phon no

        phone_lable1=Label(student_frame,text="Phone NO:",font=("times new roman",13,"bold"),bg="white")
        phone_lable1.grid(row=3,column=2,padx=10,pady=5,sticky=W)

        phone_entry=ttk.Entry(student_frame,textvariable=self.var_phone,width=20,font=("times new roman",13,"bold"))
        phone_entry.grid(row=3,column=3,padx=10,pady=5,sticky=W)

        #ADDRESS

        add_lable1=Label(student_frame,text="Address:",font=("times new roman",13,"bold"),bg="white")
        add_lable1.grid(row=4,column=0,padx=10,pady=5,sticky=W)

        add_entry=ttk.Entry(student_frame,textvariable=self.var_add,width=20,font=("times new roman",13,"bold"))
        add_entry.grid(row=4,column=1,padx=10,pady=5,sticky=W)

        #teacher name

        teacher_lable1=Label(student_frame,text="Teacher Name :",font=("times new roman",13,"bold"),bg="white")
        teacher_lable1.grid(row=4,column=2,padx=10,pady=5,sticky=W)

        teacher_entry=ttk.Entry(student_frame,textvariable=self.var_teacher,width=20,font=("times new roman",13,"bold"))
        teacher_entry.grid(row=4,column=3,padx=10,pady=5,sticky=W)

        # radio button
        self.var_radio1=StringVar()
        radiobtn1=ttk.Radiobutton(student_frame,variable=self.var_radio1,text="Take Photo Sample",value="YAS")
        radiobtn1.grid(row=6,column=0)
        
        radiobtn2=ttk.Radiobutton(student_frame,variable=self.var_radio1,text="No Photo Sample",value="NO")
        radiobtn2.grid(row=6,column=1)

        #buttob frame
        btn_frame=Frame(student_frame,bd=2,relief=RIDGE,bg="white")
        btn_frame.place(x=0,y=200,width=715,height=35)

        save_frame=Button(btn_frame,text="Save",command=self.add_data,width=17,font=("times new roman",13,"bold"),bg="blue")
        save_frame.grid(row=0,column=0)

        update_frame=Button(btn_frame,text="Update",width=17,font=("times new roman",13,"bold"),bg="blue")
        update_frame.grid(row=0,column=1)

        delete_frame=Button(btn_frame,text="Delete",width=17,font=("times new roman",13,"bold"),bg="blue")
        delete_frame.grid(row=0,column=2)

        reset_frame=Button(btn_frame,text="Reset",width=17,font=("times new roman",13,"bold"),bg="blue")
        reset_frame.grid(row=0,column=3)


        btn_frame1=Frame(student_frame,bd=2,relief=RIDGE,bg="white")
        btn_frame1.place(x=0,y=235,width=715,height=35)

        take_photo=Button(btn_frame1,text="Take Photo Sample",width=35,font=("times new roman",13,"bold"),bg="blue")
        take_photo.grid(row=0,column=0)

        update_photo=Button(btn_frame1,text="Update Photo Sample",width=35,font=("times new roman",13,"bold"),bg="blue")
        update_photo.grid(row=0,column=1)

        #right lable

        right_fream=LabelFrame(main_fream,bd=2,bg="white",relief=RIDGE,text="Student Details",font=("times new roman",12,"bold"))
        right_fream.place(x=750,y=10,width=720,height=580)

        img_right=Image.open(r"C:\Users\mahiv\OneDrive\Pictures\ALLpHOTO\left2.jpeg")
        img_right=img_right.resize((720,130),Image.Resampling.LANCZOS)
        self.Photoimg_right=ImageTk.PhotoImage(img_right)

        f_lbl=Label(right_fream,image=self.Photoimg_right)
        f_lbl.place(x=5,y=0,width=720,height=130)

        # ========Search System ================

        search_frame=LabelFrame(right_fream,bd=2,bg="white",relief=RIDGE,text="Current Course",font=("times new roman",12,"bold"))
        search_frame.place(x=5,y=135,width=710,height=70)

        search_lable1=Label(search_frame,text="Search BY:",font=("times new roman",15,"bold"),bg="red")
        search_lable1.grid(row=0,column=0,padx=10,pady=5,sticky=W)

        search_combo=ttk.Combobox(search_frame,font=("times new roman",13,"bold"),state="readonly",width=20)
        search_combo["value"]=("Select ","Roll NO","phon no")
        search_combo.current(0)          
        search_combo.grid(row=0, column=1,padx=2,pady=10,sticky=W)

        search_entry=ttk.Entry(search_frame,width=15,font=("times new roman",13,"bold"))
        search_entry.grid(row=0,column=2,padx=10,pady=5,sticky=W)

        search_frame=Button(search_frame,text="Search",width=15,font=("times new roman",12,"bold"),bg="blue")
        search_frame.grid(row=0,column=3,padx=4)

        showall_frame=Button(search_frame,text="Show ALL",width=15,font=("times new roman",12,"bold"),bg="blue")
        showall_frame.grid(row=0,column=4,padx=4)

        # ======table frame ===============

        table_frame=Frame(right_fream,bd=2,bg="white",relief=RIDGE)
        table_frame.place(x=5,y=210,width=710,height=350)

        scroll_x=ttk.Scrollbar(table_frame,orient=HORIZONTAL)
        scroll_Y=ttk.Scrollbar(table_frame,orient=VERTICAL)

        self.student_table=ttk.Treeview(table_frame,columns=("dep","course","year","sem","id","Name","div","roll no","gender","phone no","add","teacher","photo"),xscrollcommand=scroll_x.set,yscrollcommand=scroll_Y.set)

        scroll_x.pack(side=BOTTOM,fill=X)
        scroll_Y.pack(side=RIGHT,fill=Y)
        scroll_x.config(command=self.student_table.xview)
        scroll_Y.config(command=self.student_table.yview)


        self.student_table.heading("dep",text="Department")
        self.student_table.heading("course",text="Course")
        self.student_table.heading("Name",text="NAME")
        self.student_table.heading("id",text="ID")
        self.student_table.heading("year",text="YEAR")
        self.student_table.heading("sem",text="SEM")
        self.student_table.heading("roll no",text="ROOL NO")
        self.student_table.heading("gender",text="GENDER")
        self.student_table.heading("div",text="DIV")
        self.student_table.heading("phone no",text="PHONE NO")
        self.student_table.heading("teacher",text="TEACHER")
        self.student_table.heading("photo",text="PHOTO")
        #self.student_table.heading("addr",text="address")
        self.student_table["show"]="headings"


        self.student_table.column("dep",width=100)
        self.student_table.column("course",width=100)
        self.student_table.column("Name",width=100)
        self.student_table.column("id",width=100)
        self.student_table.column("year",width=100)
        self.student_table.column("sem",width=100)
        self.student_table.column("roll no",width=100)
        self.student_table.column("gender",width=100)
        self.student_table.column("div",width=100)
        self.student_table.column("phone no",width=100)
        self.student_table.column("teacher",width=100)
        self.student_table.column("photo",width=100)
        self.student_table.column("add",width=100)
    
        self.student_table.pack(fill=BOTH,expand=1)


        # ==========function ===========
    def add_data(self):
        if self.var_dep.get()=="Select Department" or self.var_name.get()=="":
            messagebox.showerror("Error","All Fielf are Required",parent=self.root)
        else:
            messagebox.showerror("Welcome with ManoramaVyas")









if __name__ == "__main__":
    root = Tk()
    obj = Student(root)
    root.mainloop()
