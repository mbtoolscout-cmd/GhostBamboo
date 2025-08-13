# Ghost Bamboo – GitHub Pages Starter (ภาษาไทย)

เทมเพลตนี้คือฐานสำหรับเว็บรีวิว/เปรียบเทียบแบบไมโครนิเช์ (ภาษาไทย) เพื่อทำ Affiliate + สินค้าดิจิทัล + POD
ใช้ Jekyll ที่ GitHub Pages สร้างหน้าให้อัตโนมัติ เปิดฟรี ไม่มีค่าโฮสต์

## โครงสร้าง
```
_config.yml             # ตั้งค่า Jekyll/ปลั๊กอิน (sitemap + feed)
_layouts/default.html   # เทมเพลตหน้าเว็บ
index.md                # หน้าแรก แสดงโพสต์ในโฟลเดอร์ posts/
posts/                  # โพสต์ Markdown ที่มี front matter
  └─ sample.md          # ตัวอย่างโพสต์ + FAQ Schema
assets/css/style.css    # สไตล์พื้นฐาน
robots.txt              # เปิดให้บอทอ่าน + ชี้ sitemap
INDEXNOW_KEY.txt        # วางค่า key สำหรับ IndexNow (ถ้าใช้)
```

## วิธีใช้งานครั้งแรก (5 นาที)
1) **สร้าง Repo ใหม่บน GitHub**
   - ชื่ออะไรก็ได้ (เช่น `bamboodeals`)
   - อัปโหลดไฟล์ทั้งหมดจากโฟลเดอร์นี้เข้าไป (หรือแตกไฟล์ ZIP แล้วลากใส่)
2) **เปิดใช้งาน GitHub Pages**
   - ไปที่ Settings → Pages → Source เลือก `Deploy from a branch`
   - Branch: `main` / Folder: `/ (root)` → กด Save
   - รอสักครู่ จะได้ URL: `https://YOUR-USERNAME.github.io/REPO-NAME`
3) **แก้ `_config.yml`**
   - ถ้าเป็น repo แบบ `YOUR-USERNAME.github.io` → ตั้ง `baseurl: ""`
   - ถ้าเป็น repo ปกติ → ตั้ง `baseurl: /REPO-NAME`
   - ตั้ง `url: https://YOUR-USERNAME.github.io`
4) **แก้ `robots.txt` (ไม่บังคับ)** ให้ชี้ Sitemap ถูกต้องตาม `url`/`baseurl`
5) **ทดสอบ** เปิดหน้าเว็บ ดูโพสต์ตัวอย่างที่หน้าแรก

## เพิ่มโพสต์ใหม่ด้วยตัวเอง
- สร้างไฟล์ใน `posts/ชื่อเรื่อง.md`
- ต้องมี front matter ด้านบน เช่น:
  ```
  ---
  title: "หูฟังไร้สาย รุ่นไหนดี"
  date: 2025-08-13
  ---
  เนื้อหา...
  ```
- ใส่ตาราง/หัวข้อ/FAQ Schema ได้ตามต้องการ

## ต่อเข้ากับสคริปต์อัตโนมัติ (Apps Script)
- ใช้โค้ดตัวอย่างในคำตอบก่อนหน้า
- ให้ `pushToGitHub(path, content)` ส่งไฟล์ไปที่โฟลเดอร์ `posts/`
  (ไม่ต้องใช้ `_posts` ก็ได้ เทมเพลตนี้อ่านจาก `posts/` โดยตรง)
- ตั้ง Trigger ให้รันทุกวันเพื่อโพสต์อัตโนมัติ

## เปิดใช้ IndexNow (ถ้าต้องการเร่งการเก็บข้อมูล)
- วางไฟล์ `INDEXNOW_KEY.txt` ด้วยค่า key จริงของคุณที่โฟลเดอร์ราก (root)
- ให้สคริปต์ไปเรียก API IndexNow พร้อม URL ของโพสต์ใหม่

## หมายเหตุสำคัญ
- หลีกเลี่ยงการอ้างอิงเกินจริง
- ระบุว่าเป็นลิงก์แนะนำ (Affiliate) หากมี
- หลีกเลี่ยงการละเมิดลิขสิทธิ์/เครื่องหมายการค้า

ขอให้ทำเงินลื่นไหลครับ 🚀