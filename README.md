# เว็บไซต์ร้านพี่ดา (ดอกไม้สด)

เว็บไซต์แบบ Static HTML พร้อมไฟล์ภาพ ใช้งานได้โดยไม่ต้องติดตั้ง dependencies หรือ build ขั้นตอนใด ๆ

## รันในเครื่อง

เปิดไฟล์ `index.html` ในเว็บเบราว์เซอร์ได้เลย หรือใช้ส่วนขยาย Live Server ใน VS Code

## Deploy ด้วย GitHub และ Vercel

1. แตกไฟล์ ZIP นี้
2. สร้าง repository ใหม่บน GitHub แล้วอัปโหลดไฟล์และโฟลเดอร์ทั้งหมด โดยให้ `index.html` อยู่ที่ root ของ repository
3. เข้า [Vercel](https://vercel.com/) แล้วเลือก **Add New → Project**
4. Import repository จาก GitHub
5. สำหรับ Framework Preset เลือก **Other** (หรือปล่อยให้ Vercel ตรวจจับเป็น Static Site) และไม่ต้องกำหนด Build Command
6. กำหนด Output Directory เป็น `.` หาก Vercel ขอให้ระบุ
7. กด **Deploy**

เมื่อเชื่อม GitHub กับ Vercel แล้ว การ push การแก้ไขครั้งถัดไปจะทำให้ Vercel deploy เวอร์ชันใหม่โดยอัตโนมัติ

## สิ่งที่แก้ไข

- ลบปุ่ม **“☎ โทรหาร้าน”** ที่มุมขวาบนในแถบเมนูออกแล้ว
- ยังคงปุ่มโทรในส่วน **ติดต่อเรา** และเบอร์โทรในรายละเอียด/ท้ายเว็บไซต์ไว้ตามเดิม
- เพิ่ม `vercel.json` สำหรับการตั้งค่าเว็บไซต์ Static

## โครงสร้างไฟล์

```text
.
├── index.html
├── vercel.json
├── README.md
└── images/
    ├── banner.png
    ├── rose-bouquet.png
    ├── marigold.png
    └── worship-flowers.png
```
