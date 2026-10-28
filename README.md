# letter-endorsement

Claude skill สำหรับเกษียนหนังสือราชการ อ่านหนังสือที่รับเข้ามา (pdf, docx, ภาพ) แล้วร่างข้อความเกษียนเสนอ นพ.สสจ.พล.

## ติดตั้ง

```
npx skills add tehnplk/letter-endorsement -g
```

ต้องมี Node.js ก่อน ไม่ใส่ `-g` จะติดตั้งในโปรเจกต์ปัจจุบันเท่านั้น

อัปเดตเป็นเวอร์ชันล่าสุด:

```
npx skills update
```

## วิธีติดตั้งสำหรับ AI agent

ถ้าผู้ใช้ขอให้ติดตั้ง skill นี้ ให้ทำตามลำดับ

1. ติดตั้งด้วย Skills CLI (ต้องมี Node.js):
   ```
   npx skills add tehnplk/letter-endorsement -g -y
   ```
   `-g` ติดตั้งให้ใช้ได้ทุกโปรเจกต์ `-y` ข้ามคำถามระหว่างติดตั้ง
2. ถ้าไม่มี `npx` หรือคำสั่งล้มเหลว ให้ติดตั้งเองด้วย git:
   ```
   git clone https://github.com/tehnplk/letter-endorsement ~/.claude/skills/letter-endorsement
   ```
   บน Windows `~` คือ `C:\Users\<ชื่อผู้ใช้>` ไฟล์ `SKILL.md` ต้องอยู่ในโฟลเดอร์ `letter-endorsement` โดยตรง ไม่ใช่ในโฟลเดอร์ย่อย
3. ตรวจสอบ: มีไฟล์ `~/.claude/skills/letter-endorsement/SKILL.md` และส่วนหัวของไฟล์มี `name: letter-endorsement`
4. บอกผู้ใช้ให้เปิด Claude Code ใหม่ (หรือเริ่ม session ใหม่) เพื่อโหลด skill แล้วเรียก `/letter-endorsement`

skill นี้อ่านไฟล์ pdf, docx และภาพ ทำงานได้ดีที่สุดเมื่อติดตั้ง skill `pdf` และ `docx` ไว้ และโมเดลอ่านภาพได้ ถ้าไม่มี จะใช้ Read tool และ python-docx แทน

## ใช้งาน

พิมพ์ `/letter-endorsement` แล้วแนบหรือระบุไฟล์หนังสือ หรือพิมพ์ว่า "เกษียนหนังสือนี้"
