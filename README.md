# scpy204_2022s2
This is a repository for students at department of Physics, Faculty of Science, Mahidol university. 

# คำชี้แจงข้อสอบปลายภาควิชา SCPY204 
จุดประสงค์สูงสุดของข้อสอบนี้คือ นักศึกษาสามารถใช้ package Matplotlib ใน python เพื่อสร้างกราฟให้หน้าตาเหมือนกราฟตัวอย่างด้านล่างนี้ 

![SCPY204_finalExam_plot](https://user-images.githubusercontent.com/52993686/235397567-575b9d16-a70a-4d79-a69f-52e18c85d6ce.png)


## คำชี้แจงอย่างละเอียด
1. เปิดไฟล์ใหม่ใน google colab โดยใช้ชื่อเป็น u64xxxxxx_NickName_final.ipynb ซึ่ง u64xxxxxx ให้ใส่รหัสนักศึกษาของตัวเองและ NickName ให้ใส่ชื่อเล่นของตัวเอง

2. ในไฟล์ที่เปิดไว้ตามข้อ 1 Clone github นี้ไป จะมีไฟล์ข้อมูลที่ต้องการอยู่ โดยใช้คำสั่งต่อไปนี้ 
```
!git clone "https://github.com/yumasr/scpy204_2022s2_finalexam.git"
```

3. ไฟล์ข้อมูลที่จะต้องใช้ มี 2 ไฟล์ คือ 
    - morishita2023_4final.csv -> เป็นข้อมูลสำหรับ 11 วัตถุ ที่จะใช้ สีแดงขอบดำ 
    - 3DHST_data_4SCPY204_finalExam.csv -> เป็นข้อมูลของ 200,000 กว่าวัตถุที่จะกำหนดสี ด้วย variable z_peak ในไฟล์ (colorbar)

4. กราฟแกน x จะเป็น log ฐาน 10 ของ stellr mass หรือ ใช้ M* แทน โดยมีหน่วยตามที่เขียนในกราฟ (เป็นจำนวนเท่าของมวลดวงอาทิตย์) 
    - มวลในทั้งสองไฟล์ ใส่ log ไว้แล้ว 
    
5. แกน y เรียกว่า Surface star formation rate ซึ่งต้องคำนวณจาก 
    - สำหรับ ไฟล์ morishita ใช้ $\Sigma_{\rm SFR} = SFR\times 10^6 / 2\pi r_e^2$
    - สำหรับ 3DHST ให้ใช้ $\Sigma_{\rm SFR} = SFR / 2\pi r_e^2$

6. สำหรับข้อมูล Morishita ใช้ error propagation ในการคำนวณความคลาดเคลื่อนของ Surface SFR 

7. plot 3D-HST data ก่อนค่อย plot Morishita data

8. ขนาดตัวอักษร
    - font ที่ใช้ระบุแกน X-Y คือ Serif ขนาด 20 แต่ตัวเลข มีขนาด 16 
    - สำหรับ แกนของ colorbar ให้ใช้ fontsize 16 และตัวเลขขนาด 14
    - ส่วนตัวอักษรที่ระบุ "JWST sources at z=7-14" ใช้ขนาด 14 
    
9. Save figure เป็นไฟล์ PNG ช่ือเดียวกับ ชื่อไฟล์ ipynb 

10. Download ไฟล์ ipynb แล้ว submit พร้อมไฟล์ภาพ ที่ google classroom 

ขอให้ทุกคนโชคดี 


หมายเหตุ เว็บที่ใช้เป็นแหล่งหาข้อมูล https://matplotlib.org/stable/gallery/lines_bars_and_markers/index.html
ลองกดดูที่รูปตัวอย่าง มันจะมี code ที่เค้าใช้ สามารถนำมาประยุกต์ใช้ได้เลย 
