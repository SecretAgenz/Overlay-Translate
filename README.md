# Overlay Translate

Translates on-screen game chat and subtitles into Thai, drawn right over the original text. Reads English, Vietnamese, Chinese, Korean and Japanese. Runs locally with Gemma 4 E2B in Docker (CPU only), nothing leaves your PC. Personal, non-commercial use only.

> **ใช้ส่วนตัว / ไม่แสวงหากำไรเท่านั้น — ห้ามนำไปขาย แจกเพื่อหากำไร หรือใช้เชิงพาณิชย์**
> (มีส่วนประกอบสัญญา CC BY-NC 4.0 คือ VieSVTR) / **Personal, non-commercial use only.**

## ภาษาไทย

แปลแชตและซับไตเติลบนหน้าจอเกมเป็นภาษาไทย แล้ววางคำแปลทับตำแหน่งข้อความเดิม โดยไม่แปลชื่อผู้เล่น

### จุดเด่น
- วาดกรอบครอบกล่องแชตครั้งเดียว แอปจำกรอบไว้ เปิดครั้งหน้าแปลอัตโนมัติเลย
- อ่านได้: อังกฤษ เวียดนาม (อ่านวรรณยุกต์ได้) จีน เกาหลี ญี่ปุ่น ตรวจภาษาอัตโนมัติ
- แปลด้วย Gemma 4 E2B ที่รันบนเครื่องคุณผ่าน Docker ใช้ CPU ไม่แย่ง VRAM ของเกม ข้อความไม่ถูกส่งออกนอกเครื่อง
- เลือกแปลเฉพาะตอนอยู่ในเกมได้ สลับโปรแกรมอื่นคำแปลหายทันที และคำแปลหายตามเมื่อแชตจางหาย
- เปิดแล้วเงียบ ควบคุมผ่านไอคอนถาดระบบและปุ่มลัด คำแปลไม่ติดในภาพหน้าจอ (มีโหมดถ่ายภาพ F11 ชั่วคราว)
- ตัวติดตั้งเดียวติดตั้งให้ครบ: แอป Docker โมเดลแปล และ OCR

### ความต้องการ
- Windows 10/11 แบบ 64 บิต, RAM 16 GB ขึ้นไป, ที่ว่างราว 10 GB
- อินเทอร์เน็ตตอนติดตั้ง และสิทธิ์ผู้ดูแลเครื่อง
- เปิด Virtualization ใน BIOS (Docker ต้องใช้)

### ติดตั้งและใช้งาน
1. ดาวน์โหลดชุดติดตั้งจากหน้า **Releases** แล้วแตก zip ให้หมด (ต้องมี `Setup.exe` กับโฟลเดอร์ `payload` ด้วยกัน)
2. ดับเบิลคลิก `Setup.exe` กดอนุญาตสิทธิ์ผู้ดูแล ติ๊กยอมรับเงื่อนไข แล้วกดติดตั้ง
3. เปิดเกม กด `Ctrl+Shift+D` ลากครอบกล่องแชต แอปจะแปลให้อัตโนมัติ หรือกด `F8` เพื่อแปลทันที

ปุ่มลัด: `Ctrl+Shift+D`/`F10` วาดกรอบใหม่ · `F8` แปลตอนนี้ · `F9` เปิด/ปิดแปลอัตโนมัติ · `F7` ซ่อน/แสดง · `F6` สลับแชต/ซับ · `F11` โหมดถ่ายภาพ · `Ctrl+Shift+Q` ปิดแอป

วิธีติดตั้งโดยละเอียดและแก้ปัญหา อยู่ในไฟล์ `README.txt` ที่มากับชุดติดตั้ง

### ข้อจำกัด
- โมเดลแปลเป็นโมเดลเล็ก ภาษาแชตแบบย่อหรือเวียดนามที่ไม่มีวรรณยุกต์อาจแปลไม่แม่น
- OCR ภาษาญี่ปุ่น/เกาหลี/จีน ยังทดสอบกับข้อความจริงน้อย

## English

Draw a box around the chat once and it is remembered. The app reads the text in the box, translates it into Thai with a small local model (Gemma 4 E2B running in Docker on the CPU, so it does not take VRAM from the game) and draws the translation over the original text. Player names are not translated. Optional "translate only while the game is active" mode. One setup installs everything.

**Requirements:** Windows 10/11 64-bit, 16 GB RAM or more, about 10 GB free disk, internet during setup, administrator rights, virtualization enabled in the BIOS.

**Limitations:** the model is small, so slang and unaccented Vietnamese may translate poorly; Japanese/Korean/Chinese OCR has had little testing on real game text.

## Licenses and third-party components

This project is for **personal, non-commercial use only**. It bundles or installs components with their own terms:

| Component | Terms |
|---|---|
| VieSVTR v7 (Vietnamese text recogniser) | CC BY-NC 4.0, non-commercial only, attribution required |
| Gemma 4 E2B | Google's Gemma Terms of Use and Prohibited Use Policy (https://ai.google.dev/gemma/terms) |
| llama.cpp | MIT |
| Docker Desktop | Docker's own terms (free for personal use) |
| Windows OCR language components | Microsoft, installed from Windows Update |

No license file is included on purpose: all rights are reserved except the use described above. This text communicates the terms to users and is not legal advice.
