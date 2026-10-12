# Fish Farm Festival — Wiki

เว็บไซต์คู่มือ/วิกิของโมดแพ็ก **Fish Farm Festival** (Minecraft 1.20.1 Fabric) เป็นเว็บ **static** ล้วน (HTML/CSS) ไม่ต้อง build เปิดได้ทันทีและ deploy ง่าย

## โครงสร้างโฟลเดอร์

```
FFF-Wiki/
├── index.html              หน้าแรก — คู่มือผู้เล่นหน้าเดียวจบ (มีสารบัญด้านข้าง)
├── README.md               ไฟล์นี้
├── .nojekyll               ให้ GitHub Pages เสิร์ฟไฟล์ตามจริง ไม่ผ่าน Jekyll
│
├── guides/                 หน้าคู่มือเชิงลึก (สำหรับผู้เล่น)
│   ├── skill-tree.html         คู่มือ Skill Tree ทุกโหนด 3 สาย
│   ├── food-system.html        ระบบอาหาร (Spice of Fabric/Diet)
│   └── fish.html               สารานุกรมปลา 158 ชนิด (ที่ไหน เวลาไหน อุปกรณ์)
│
├── design/                 เอกสารออกแบบ/ภายใน (ไม่ใช่หน้าเผยแพร่หลัก)
│   ├── festival.html           ดีไซน์ระบบเทศกาล
│   ├── economy.html            ดีไซน์เศรษฐกิจ
│   ├── progression.html        ดีไซน์สาย progression
│   ├── release-1.3-audit.html  รายงานตรวจก่อนปล่อย 1.3
│   └── angler-skills-legacy.html  คู่มือ Angler เวอร์ชันเก่า (ก่อนรีบาลานซ์ 1.3.1)
│
├── content/                ต้นฉบับข้อความ (Markdown)
│   ├── pack-description.md      คำอธิบายแพ็กสำหรับหน้า CurseForge
│   ├── core-mod-page.md        คำอธิบายมอด Fish Farm Festival Core
│   └── changelogs/
│       ├── changelog-1.3.md
│       └── changelog-1.3.1.md
│
├── downloads/              ไฟล์ให้ดาวน์โหลด
│   └── fish-farm-festival-core-1.3.1.jar
│
└── assets/                 ทรัพยากรเว็บ (เตรียมไว้สำหรับพัฒนาต่อ)
    ├── css/                    สไตล์ชีตรวม (ยังว่าง — ดู "ขั้นตอนต่อไป")
    └── img/                    รูปภาพ โลโก้ สกรีนช็อต
```

## วิธีดู
ดับเบิลคลิก `index.html` เปิดในเบราว์เซอร์ได้เลย หรือรันเซิร์ฟเวอร์ static ในโฟลเดอร์นี้:

```
python -m http.server 8000
```

แล้วเปิด `http://localhost:8000`

## วิธี Deploy (เลือกอย่างใดอย่างหนึ่ง)
- **GitHub Pages:** push โฟลเดอร์นี้ขึ้น repo แล้วเปิด Pages ชี้ที่ root (มี `.nojekyll` อยู่แล้ว)
- **Netlify / Cloudflare Pages / Vercel:** ลากโฟลเดอร์ทั้งก้อนวาง ตั้ง build command ว่าง และ publish directory เป็น root
- ทุกหน้าเป็นไฟล์เดี่ยวจบในตัว (CSS ฝังในไฟล์) จึงเปิด/เสิร์ฟได้โดยไม่ต้องตั้งค่าอะไรเพิ่ม

## สถานะปัจจุบัน
- ทุกหน้าเป็น HTML เดี่ยว ฝัง CSS ไว้ในไฟล์ รองรับ dark/light ตามระบบ ฟอนต์ไทย Sarabun
- `index.html` มีสารบัญด้านข้าง + ส่วน "คู่มือเชิงลึก" ลิงก์ไปหน้าใน `guides/`
- หน้าใน `guides/` และ `design/` ยังไม่มีเมนูกลับหน้าแรก (เปิดดูเดี่ยวได้)

## ขั้นตอนต่อไป (ถ้าจะพัฒนาเป็นเว็บจริง)
1. **แยก CSS ที่ซ้ำกันออกมาเป็น `assets/css/site.css`** แล้วให้ทุกหน้า `<link>` มาใช้ร่วมกัน (ตอนนี้แต่ละหน้าฝัง CSS ของตัวเอง ธีมคล้ายกันอยู่แล้ว รวมได้)
2. **ทำแถบเมนู/ส่วนหัวร่วม (header/nav)** ให้ทุกหน้า แล้วมีลิงก์กลับหน้าแรกและข้ามไปหน้าอื่น
3. **ใส่รูปใน `assets/img/`** โลโก้ สกรีนช็อตเทศกาล แผนที่สกิลทรี เพื่อให้หน้าน่าสนใจ
4. **แปลง Markdown ใน `content/` เป็นหน้าเว็บ** (เช่น หน้า changelog, หน้าดาวน์โหลด) หรือใช้ตัว generate static site
5. **หน้าดาวน์โหลด** ลิงก์ไป CurseForge และ/หรือไฟล์ใน `downloads/`
6. พิจารณาใช้ static site generator (เช่น Astro, Eleventy, MkDocs) ถ้าเนื้อหาเริ่มเยอะและอยากมี template ร่วม

## หมายเหตุ
- ไฟล์ `.jar` ใน `downloads/` เป็นสำเนามอด Core ตัวจริงเผยแพร่บน CurseForge แล้ว
- เอกสารใน `design/` เป็นบันทึกการออกแบบระหว่างพัฒนา เก็บไว้อ้างอิง ไม่จำเป็นต้องเผยแพร่
