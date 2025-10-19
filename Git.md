# Git bilan tanishish

## git ni loyihaga initsializatsiya qilish

joriy papkada git repozitoriy hosil qilish:

```bash
git init
```

papkalar va fayllar trukturasi:

```bash
tree /a
```

## git config - git sozlamalari

git sozlamalari ro'yhati:

```bash
git config --list
```

foydalanuvchi nomini chiqaradi:

```bash
git config user.name
```

joriy kompyuter foydalanuvchisi (user) nomini kiritish:

```bash
git config --system user.name "user_name"
```

global foydalanuvchi nomini kiritish:

```bash
git config --global user.name "user_name"
```

loyiha uchun foydalanuvchi nomini kiritish (default):

```bash
git config --local user.name "project_user_name"
```

foydalanuvchi nomini o'chirish:

```bash 
git config --unset user.name
```

foydalanuvchi email ini o'chirish:

```bash
git config --unset user.email
```

sozlamalardagi user seksiyasidagi kiritilganlarni o'chirish:

```bash
git config --remove-section user
```

git commit yozish uchun matn muharririni tanlash:

```bash
git config --global -core.editor "program/path"
```

git config ni git c deb alias bilan qisqartirishni sozlash, config = c:

```bash
git config --global alias.c config
```

git sozlamalari haqida yordam ma'lumotlari olish:

```bash
git config -h
```

git haqida asosiy yordam:

```bash
git help
```

sozlamalar haqida yordam:

```bash
git help config
```

---

## Repozitoriy hosil qilish va birinchi commit

loyiha holati haqida ma'lumotlar (gitga qo'shilmagan, yangi qo'shilgan, o'chirilgan va o'zgargan fayllar ro'yhati):

```bash
git status
```

barcha fayllarni git indexga qo'shish:

```bash
git add . 
```

shu nomli faylni git index ga qo'shish:

```bash
git add "file_name"
```

git config --global core.editor "editor/full/path" sozlamasida kiritilgan editor orqali commit xabari yozish:


```bash
git commit
```

qisqa_sarlavha     1-qator (50 belgidan oshmasin)

bo'sh_qator

batafsil_tavsif    ixtiyoriy, lekin foydali

Katta loyihalarda sarlavha oldiga turini ko‘rsatish qulay bo‘ladi:

```text
Prefiks     Ma'nosi
feat:       Yangi funksiya qo'shildi
fix:        Xato tuzatildi
refactor:   Kod yaxshilandi (funksional o'zgarmadi)
style:      Faqat dizayn yoki formatlash o'zgarishi
docs:       Hujjatlar (README, izohlar) o'zgardi
test:       Testlar qo'shildi yoki o'zgardi
```

Misollar:

```bash
git commit -m "feat: Qo‘sh yangi foydalanuvchi ro‘yxatdan o‘tish sahifasi"
git commit -m "fix: Tuzat so‘rov yuborishda xato chiqishini"
git commit -m "refactor: Soddalashtir kodni o‘qish uchun"
git commit -m "style: Navbar rangini o‘zgartir"
```

index ga kiritilgan qisqa commitlarga o'zgarish haqida ma'lumot yozish, git add qilingan fayl(lar)ga commit xabar kiritish:

```bash
git commit -m "commit xabar"
```

---

## Git va fayllarga bo'lgan huquq

```text
bu mavzu hozirda uncha muhim emas
4-videodarsda tushuntirilgan
```

---

## git show, muallif va committer

muallif - kodni 1-yozgan odam,

commiter - kodni yangilab yozgan va commit qilgan odam

shu commit haqida to'liq ma'lumotlarni ko'rish:

```bash
git show 'commit_hash_code'
```

boshqacharoq kengaytirilgan ko'rinishda:

```bash
git show --pretty=fuller cc2ada60b3d71482638103b9ccdbe14d957c254c
```

shu nomli muallifning (commiter emas, author) commitini yozish:

```bash
git commit --author='John <john@mail.uz>'
```

---

## Fayllar va direktoriyalar yaratish, git status

joriy papkadagi barcha fayllarni git index ga qo'shish:

```bash
git add .
```

.gitignore dan qat'iy nazar index ga qo'shish:

```bash
git add -force '.idea/project.iml'
```

yoki

```bash
git add -f '.idea/project.iml' 
```

Root dagi .idea papkasini indexdan olib tashlash:

```bash
git reset HEAD .idea
```
