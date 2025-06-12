[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-22041afd0340ce965d47ae6ef1cefeee28c7c493a6346c4f15d667ab976d596c.svg)](https://classroom.github.com/a/w8H8oomW)

**<ins>Note</ins>: Students must update this `README.md` file to be an installation manual or a README file for their own CS403 projects.**

**รหัสโครงงาน:** 67-1_35_snk-s1

**ชื่อโครงงาน (ไทย):** การศึกษาเชิงเปรียบเทียบการสรุปข้อมูลจากสื่อมัลติมิเดียด้านสุขภาพโดยใช้ปัญญาประดิษฐ์

**Project Title (Eng):** A COMPARATIVE STUDY OF SUMMARIZING HEALTH INFOGRAPHIC USING ARTIFICIAL INTELLIGENCE

**อาจารย์ที่ปรึกษาโครงงาน:** ผศ.ดร. ศาตนาฏ กิจศิรานุวัตร

**ผู้จัดทำโครงงาน:** 
1. นายธนดล สายคำพัน 6309650460  thanadol.say@dome.tu.ac.th


## Table of Contents

- [ชุดโปรแกรมที่ต้องติดตั้ง](#ชุดโปรแกรมที่ต้องติดตั้ง)
- [ไลบรารีและโมเดลที่ต้องติดตั้ง](#ไลบรารีและโมเดลที่ต้องติดตั้ง)
- [วิธีการติดตั้งระบบ](#วิธีการติดตั้งระบบ)
- [การใช้งานระบบ](#การใช้งานระบบ)
- [หมายเหตุ](#หมายเหตุ)

---

## โปรแกรมที่ต้องติดตั้ง

1. [**Python 3.8**](https://www.python.org/downloads/)
2. [**Ollama**](https://ollama.com/download)
3. [**Docker Desktop**](https://www.docker.com/products/docker-desktop) 
4. [**Jupyter Notebook**](https://jupyter.org/install)

---

##  ไลบารี่และโมเดลที่ต้องติดตั้ง

### ไลบารี่
Tesseract OCR 5.5.0

###  AI Models 
llama3.2-vision:11b
gemma:7b

----------

## วิธีการติดตั้งระบบ

### 1. ติดตั้งโปรแกรมที่ต้องการติดตั้ง

Python 3.8
วิธีติดตั้ง Python บน **Windows**

ขั้นตอนที่ 1 ดาวน์โหลดตัวติดตั้ง
1. ดาวน์โหลดตัวติดตั้ง Python
2.  กดปุ่ม Download Python 3.8.0
    ตัวติดตั้งเป็นไฟล์ .exe
    
เริ่มติดตั้ง

1.  ดับเบิ้ลคลิกไฟล์ `.exe` ที่ดาวน์โหลดมา
2.  ก่อนกด Install ให้ทำเครื่องหมายถูกหน้า Add Python 3.8.0 to PATH       
3.  คลิก Install Now
   
ตรวจสอบการติดตั้ง

หลังติดตั้งเสร็จ ให้เปิด Command Promptแล้วพิมพ์

```bash
python --version 
```

หรือ:


```bash
python
```
Ollama
1.  เข้าเว็บไซต์ Ollama: 
   
2.  เลือกไฟล์ติดตั้งตามระบบปฏิบัติการของคุณ:
    
    -   **Windows**
        
    -   **macOS**
        
    -   **Linux**
        
3.  ดาวน์โหลดไฟล์ และติดตั้ง
        
4.  เมื่อติดตั้งเสร็จแล้ว โปรแกรมจะรัน background service อัตโนมัติ

Docker Desktop
1. กดปุ่ม **“Download for Windows”** 
    
2. ดับเบิลคลิกไฟล์ `Docker Desktop Installer.exe`
    
2.  คลิก “OK” หรือ “Yes” เมื่อ Windows ถามเรื่องสิทธิ์การติดตั้ง
    
3.  รอให้ติดตั้งเสร็จ แล้วคลิก “Close and Restart” 
    
4.  เปิด Docker Desktop จาก Start Menu
 
5.  Docker จะเริ่มทำงาน 

Jupyter Notebook

ใช้คำสั่ง
```bash
pip install notebook
```
หลังจากนั้นทำการรันด้วยคำสั่ง
```bash
jupyter notebook
```

### 2. ดาวน์โหลดไลบารี่และโมเดลที่ใช้

Libaries

```bash
import pytesseract
pytesseract.pytesseract.tesseract_cmd =  r"เส้นทางไปยังไฟล์ที่ต้องการ"

pip install pytesseract

แล้วทำการ Clone Code จาก GitHub ไฟล์ OCR
```
AI Models 

```bash
ollama pull llama3.2-vision:11b
ollama pull gemma:7b
```
----------

## การใช้งานระบบ

### 1. เตรียมข้อมูล
- เตรียมชุดข้อความ OCR    
1 ให้นำภาพมาอยู่ในโฟลเดอร์เดียวกับไฟล์โค้ด OCR 
2 ทำการรันเซลจะได้ข้อความที่เป็น OCR ออกมา

### 2. รันการทดลอง
วิธีการแรก
-   วางไฟล์อินโฟกราฟฟิกจากในโฟลเดอร์ 
-   เขียนคำถามไว้ตามที่ต้องการใช้งาน

วิธีการที่สอง

- เตรียมชุดข้อความ OCR    
- เขียนคำถามที่เหมือนกันไว้


วิธีการที่สาม

- ตรวจสอบแก้ไขข้อความ OCR ที่ผิดพลาด
- เขียนคำถาม

---
## หมายเหตุ

-   หากโมเดลมีปัญหา เช่น ไม่โหลดหรือรันไม่ได้ ให้ใช้คำสั่ง
    
```bash
ollama rm gemma:7b
ollama pull gemma:7b

ollama rm llama3.2-vision:11b
ollama pull llama3.2-vision:11b
```

-   หาก Jupyter Notebook ไม่สามารถรันได้ให้พิมพ์คำสั่งใน cmd  

 ```bash
 cd [ตำแหน่งของไฟล์ที่ Jupyter notebook อยู่] 
```
    
----------
