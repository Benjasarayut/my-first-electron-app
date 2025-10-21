สรุป: Lab 8.1 – Electron.js เบื้องต้น
🎯 เป้าหมายของ Lab

ฝึกสร้าง Desktop Application ด้วย Electron.js โดยใช้เทคโนโลยี Web (HTML, CSS, JavaScript)

📘 เนื้อหาหลักที่เรียนรู้

รู้จัก Electron.js และโครงสร้างหลักของมัน

เข้าใจความแตกต่างระหว่าง Main Process และ Renderer Process

สร้างโปรเจกต์ Electron แรกได้ด้วยคำสั่ง npm start

ออกแบบ UI และเพิ่มฟังก์ชันด้วย HTML, CSS, JS

เรียนรู้วิธีรันและทดสอบ Desktop App บนเครื่องจริง
```
⚙️ โครงสร้างโปรเจกต์
my-first-electron-app/
├── main.js          # Main Process - ควบคุมหน้าต่างแอป
├── index.html       # Renderer Process - ส่วนแสดงผล UI
├── package.json     # ข้อมูลโปรเจกต์และสคริปต์รัน
└── node_modules/    # ขึ้นตอนติดตั้งอัตโนมัติ
```
🛠️ ขั้นตอนการทำงาน
1️⃣ สร้างและตั้งค่าโปรเจกต์
```
mkdir my-first-electron-app
cd my-first-electron-app
npm init -y
npm install electron --save-dev
```


แก้ไข package.json:
```
{
  "main": "main.js",
  "scripts": {
    "start": "electron ."
  }
}
```
2️⃣ เขียนโค้ด main.js

สร้าง window ด้วย BrowserWindow และโหลดไฟล์ index.html
ควบคุมการเปิด-ปิดแอปในแต่ละแพลตฟอร์ม

3️⃣ เขียนโค้ด index.html

สร้าง UI ด้วย HTML + CSS พร้อมปุ่ม 3 ปุ่ม:

🎉 Click Me → แสดงข้อความ

⏰ Show Time → แสดงเวลา

🎨 Change Color → เปลี่ยนสีพื้นหลัง

และแสดงข้อมูล system (OS, ภาษา, หน้าจอ)

4️⃣ รันแอป
npm start


✅ สิ่งที่ควรเห็น:

หน้าต่าง Desktop App เปิดขึ้น

ปุ่มกดได้จริง

ข้อมูลระบบแสดงถูกต้องในหน้าจอ

Console มี log ข้อความจากทั้ง main และ renderer process

🧠 Concept สำคัญ
ส่วน	หน้าที่	เปรียบเทียบกับ Web
Main Process	ควบคุม lifecycle และ window	Backend
Renderer Process	แสดง UI, จัดการ event	Frontend

ลำดับการทำงาน:

npm start → Electron เริ่มทำงาน
→ main.js สร้าง BrowserWindow
→ โหลด index.html
→ Renderer แสดง UI และรับ event

🧩 Assignment

ให้นักศึกษาปรับแต่งโปรเจกต์:

🎨 ปรับ UI และเพิ่มปุ่มใหม่อย่างน้อย 2 ปุ่ม

⚙️ เพิ่มฟังก์ชันใหม่ เช่น คำนวณเลข หรือแสดงวันที่

🖼️ ปรับขนาด window และใส่ icon ของ app

ส่งงานเป็น:

📁 โปรเจกต์ทั้งหมด

📸 Screenshot ของแอป

📝 รายงานสิ่งที่ปรับแต่ง

🏆 สรุปสิ่งที่เรียนรู้

สร้าง Desktop App ด้วย HTML + CSS + JS

เข้าใจ Main / Renderer Process

รู้จักการจัดการไฟล์ package.json

รู้วิธีรันและทดสอบแอปในเครื่อง

พร้อมต่อยอดไปสู่ Lab 8.2–8.4

💡 Keyword สำคัญ:

Electron = Web + Desktop
Main = Backend, Renderer = Frontend
เขียนครั้งเดียว รันได้ทุกระบบ 🌍
