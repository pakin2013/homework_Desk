# Homework Desk

เว็บจัดการรายการการบ้านแบบ static ใช้ `homework.json` เป็นข้อมูลตั้งต้น และเก็บข้อมูลที่เพิ่มหรือแก้ไขไว้ใน Local Storage ของเบราว์เซอร์

## เปิดใช้งานในเครื่อง

เปิดโฟลเดอร์ผ่านเว็บเซิร์ฟเวอร์แบบ static เพื่อให้หน้าเว็บโหลดไฟล์ JSON ได้ เช่น:

```powershell
python -m http.server 8000
```

จากนั้นเปิด <http://localhost:8000>

## เผยแพร่ด้วย GitHub Pages

GitHub Actions ใน `.github/workflows/deploy.yml` จะเผยแพร่เว็บเมื่อ push ไปยัง `main` หรือสั่ง workflow ด้วยตนเอง จากนั้นเปิด URL ใน environment `github-pages` ของ workflow ที่สำเร็จ

ข้อมูลใน Local Storage ผูกกับเบราว์เซอร์และ origin ของเว็บ ไม่ได้ซิงค์ระหว่างอุปกรณ์หรือผู้ใช้คนอื่น และการล้างข้อมูลเว็บไซต์จะลบรายการที่แก้ไขไว้ สำหรับเริ่มจากข้อมูลตัวอย่างอีกครั้ง ให้ลบคีย์ `homework-desk-data-v1` จาก Local Storage ของเว็บไซต์
