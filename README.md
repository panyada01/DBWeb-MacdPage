# **ระบบบริการนักศึกษา (Student Service System)**

โปรเจค **ระบบบริการนักศึกษา** เป็นเว็บแอปพลิเคชันที่พัฒนาด้วย **PHP** และ **MySQL**
สำหรับจัดการข้อมูล **นักศึกษา**, **คณะ**, และ **สาขาวิชา**
โดยมีการแบ่งสิทธิ์การใช้งานระหว่าง **ผู้ดูแลระบบ** และ **ผู้ใช้งานทั่วไป (นักศึกษา)**
เพื่อให้การแสดงผลและการจัดการข้อมูลเป็นไปอย่าง **มีประสิทธิภาพ**

> 💡 ระบบนี้ถูกพัฒนาขึ้นเพื่อใช้ในการเรียนรายวิชาพัฒนาเว็บแอปพลิเคชัน
> พร้อมโครงสร้างไฟล์ที่ชัดเจน และสามารถต่อยอดพัฒนาเพิ่มเติมได้

---
<p align="center">
<img width="1920" height="1080" alt="mdc1" src="https://github.com/user-attachments/assets/bc0800e4-6e5d-44ee-8899-8bbe45d725b7" width="600"/>
  <img width="1920" height="1080" alt="mdc2" src="https://github.com/user-attachments/assets/1e785fb1-3a35-4fa7-b034-c8ff09f3a28e" width="600"/>

</p>

---

## 🧩 ฟีเจอร์หลักของระบบ

### 1. ระบบล็อกอิน (Login System) ✅

รองรับการเข้าสู่ระบบของนักศึกษาและผู้ดูแลระบบ
เพื่อเข้าถึงข้อมูลตาม **สิทธิ์การใช้งาน**

---

### 2. หน้าหลักหลังเข้าสู่ระบบ (Dashboard) ✅

หลังจากล็อกอินสำเร็จ ผู้ใช้จะพบกับ **หน้าเมนูนำทางด้านซ้าย (Sidebar Navigation)**
<p align="center">
<img width="1920" height="1080" alt="mdc3" src="https://github.com/user-attachments/assets/e3073d9c-e496-4464-af18-3031f906d132" width="600"/>
  <img width="1920" height="1080" alt="mdc11" src="https://github.com/user-attachments/assets/cdb2690d-5d9e-422c-993a-225d075261be" width="600"/>
<img width="1920" height="1080" alt="mdc10" src="https://github.com/user-attachments/assets/ddb3eb49-60cc-4db4-8d28-e3cc1c10be1d"width="600" />
<img width="1920" height="1080" alt="mdc9" src="https://github.com/user-attachments/assets/2d360baf-4695-47a7-866f-73c240794d33" width="600"/>
<img width="1920" height="1080" alt="mdc8" src="https://github.com/user-attachments/assets/67bac819-7b86-4a72-93fd-6ecb7aae5f1f" width="600"/>
<img width="1920" height="1080" alt="mdc7" src="https://github.com/user-attachments/assets/8aa9f863-1178-481c-a090-730a6c26238f" width="600"/>
<img width="1920" height="1080" alt="mdc6" src="https://github.com/user-attachments/assets/7f95d429-3fb7-46a6-976b-873d4a0b7fd3" width="600"/>
<img width="1920" height="1080" alt="mdc5" src="https://github.com/user-attachments/assets/5238cb4e-02ea-4a0b-97f6-a0e58d9ae592" width="600"/>
<img width="1920" height="1080" alt="mdc4" src="https://github.com/user-attachments/assets/4f16637b-cf55-4760-a290-64ce95715104" width="600"/>

</p>

#### เมนูประกอบด้วย

* **Home**: หน้าแรกหลังเข้าสู่ระบบ แสดงข้อมูลสรุปหรือประกาศต่าง ๆ
* **ข้อมูลคณะ**: แสดงรายละเอียดของคณะในมหาวิทยาลัย เช่น ชื่อคณะ และข้อมูลที่เกี่ยวข้อง
* **ข้อมูลสาขา**: แสดงรายละเอียดของสาขาวิชาต่าง ๆ
* **ข้อมูลนักศึกษา**: แสดงข้อมูลส่วนตัวของนักศึกษา เช่น ชื่อ-นามสกุล, รหัสนักศึกษา, เบอร์โทรศัพท์ ฯลฯ
* **แผนที่ (Map)**: แสดงตำแหน่งอาคารหรือคณะในมหาวิทยาลัย เพื่อช่วยให้ผู้ใช้งานสามารถค้นหาสถานที่ได้ง่ายขึ้น
* **ออกจากระบบ (Logout)**: สำหรับออกจากระบบอย่างปลอดภัย

> ⚠️ เมนูทั้งหมดถูกออกแบบให้ **ใช้งานง่าย** พร้อม **ไอคอนประกอบ** เพื่อเพิ่มความชัดเจนและสะดวกในการนำทาง

---

> 🗂️ **โครงสร้างไฟล์หลัก**
>
> ```
> /admin            - หน้าจัดการข้อมูลสำหรับผู้ดูแลระบบ
> /user             - ส่วนแสดงข้อมูลสำหรับผู้ใช้งานทั่วไป
> /components       - ส่วนประกอบซ้ำ เช่น header, footer, navbar
> /assets           - ไฟล์รูปภาพ ไอคอน และสไตล์
> /database         - ไฟล์เชื่อมต่อฐานข้อมูล (config)
> ```

---

## 🎯 วัตถุประสงค์ของโปรเจค

* ฝึกการสร้าง **เว็บแอปพลิเคชันด้วย PHP** และ **ฐานข้อมูล MySQL**
* แบ่งส่วนการทำงานของระบบ **ผู้ดูแล** และ **ผู้ใช้งานทั่วไป**
* สามารถ **ต่อยอดเพิ่มการจัดการข้อมูลอื่น ๆ** ในอนาคตได้

---

