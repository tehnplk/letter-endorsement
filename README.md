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

## Installation instructions for AI agents

If a user asks you to install this skill, follow these steps in order.

1. Install with the Skills CLI (needs Node.js):
   ```
   npx skills add tehnplk/letter-endorsement -g -y
   ```
   `-g` installs for all projects, `-y` skips the prompts.
2. If `npx` is unavailable or the command fails, install manually with git:
   ```
   git clone https://github.com/tehnplk/letter-endorsement ~/.claude/skills/letter-endorsement
   ```
   On Windows `~` is `C:\Users\<user>`. The folder must contain `SKILL.md` directly, not inside a subfolder.
3. Verify: `~/.claude/skills/letter-endorsement/SKILL.md` exists and its frontmatter has `name: letter-endorsement`.
4. Tell the user to restart Claude Code (or start a new session) so the skill is loaded, then run `/letter-endorsement`.

The skill reads pdf, docx and image files. It works best when the `pdf` and `docx` skills are installed and the model can read images; without them it falls back to the Read tool and python-docx.

## ใช้งาน

พิมพ์ `/letter-endorsement` แล้วแนบหรือระบุไฟล์หนังสือ หรือพิมพ์ว่า "เกษียนหนังสือนี้"
