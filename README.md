# 🔐 Switch Dashboard

ระบบกันขโมยตรวจจับการเข้า-ออกของอาคาร Workshop ในรูปแบบ Web Application สำหรับตรวจสอบสถานะการทำงานของอุปกรณ์และแสดงผลข้อมูลแบบ Real-time

---

## 📖 ภาพรวมระบบ

ระบบประกอบด้วยอุปกรณ์ ESP32 จำนวน 2 บอร์ด ได้แก่

- **Write Board** : รับข้อมูลจาก Sensor และบันทึกข้อมูลลง Google Sheets
- **Read Board** : อ่านข้อมูลจาก Google Sheets และควบคุมอุปกรณ์แสดงผล
- **Web Application** : แสดงผลสถานะและข้อมูลการทำงานของระบบ

---

## 📝 Write Board

หน้าที่ของบอร์ด Write คือ

- รับข้อมูลจาก Sensor
- ประมวลผลสถานะการตรวจจับ
- ส่งข้อมูลไปจัดเก็บใน Google Sheets

### ข้อมูลที่บันทึก

| รายการ | รายละเอียด |
|----------|----------|
| MAC Address | หมายเลขประจำเครื่อง |
| Date/Time | วันและเวลา (DD/MM/YYYY HH:MM:SS) |
| Switch Status | สถานะของสวิตช์หรือเซนเซอร์ |

---

## 📥 Read Board

หน้าที่ของบอร์ด Read คือ

- ส่ง MAC Address ของอุปกรณ์
- อ่านข้อมูลจาก Google Sheets
- ประมวลผลข้อมูลที่ได้รับ
- ควบคุมอุปกรณ์ Output

### การแสดงผล

- Revolving Light (ไฟหมุนแจ้งเตือน)
- สถานะการทำงานของระบบ
- สถานะการตรวจจับการเข้า-ออก

---

## 🌐 Web Application

Web Application ใช้สำหรับ

- แสดงสถานะการทำงานของระบบ
- แสดงข้อมูลการตรวจจับแบบ Real-time
- แสดงจำนวนการเข้า-ออก
- แสดงโซนที่เกิดการตรวจจับ
- แสดงข้อมูลย้อนหลังจาก Google Sheets

---

## 🔄 Workflow การทำงาน

```text
Sensor
   │
   ▼
Write Board
   │
   ▼
Google Sheets
   │
   ▼
Read Board
   │
   ├──► Revolving Light
   │
   ▼
Web Application Dashboard
```

---

## 🛠️ Technologies Used

- ESP32
- Google Sheets API
- Web Application
- HTML / CSS / JavaScript
- Wi-Fi Communication

---

## 🎯 Objective

พัฒนาระบบตรวจจับการเข้า-ออกอาคาร Workshop
เพื่อเพิ่มความปลอดภัยและสามารถตรวจสอบสถานะการทำงานผ่าน Dashboard ได้แบบออนไลน์

---

## 👨‍💻 Developer

พัฒนาเพื่อใช้ในการศึกษาและทดสอบระบบ IoT สำหรับงานรักษาความปลอดภัย
