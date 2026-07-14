# Build Base Digitally — Tools Dashboard

Yeh repo aapke sabhi internal/client-facing tools ko **ek hi jagah** rakhta hai — GitHub se Vercel pe deploy hoga, aur ek hi memorable link (`tools.buildbasedigitally.com`) pe sab kuch milega।

---

## 📁 Folder Structure

```
bbd-tools/
├── index.html                 ← Dashboard (home page, sab tools ke links)
├── package-selector/
│   └── index.html             ← ✅ Ready (aapki Package Selector already yahan daal di hai)
├── onboarding-form/
│   └── index.html             ← ⚠️ Placeholder — apni asli file se replace karein
├── prompt-generator/
│   └── index.html             ← ⚠️ Placeholder — apni asli file se replace karein
└── checklist/
    └── index.html             ← ⚠️ Placeholder — apni asli Checklist file se replace karein
```

---

## 🔧 Step 1 — Apni Baaki Files Replace Karein

Jo bhi 3 tools aapne khud bana rakhe hain (Onboarding Form, Prompt Generator, Checklist), unki **HTML file ka naam `index.html` rakh kar**, respective folder mein daal dein (jo already wahan hai use overwrite kar dein)।

**Important:** File ka naam hamesha `index.html` hi hona chahiye — isse folder khulte hi wo page automatically dikhega।

---

## 🐙 Step 2 — GitHub Par Upload Karein (Mobile-Friendly Tarika)

Chunki aap zyada tar mobile pe kaam karte hain, yeh **bina git command ke, seedha browser se** karne ka tarika hai:

1. **github.com** pe jaake login karein (account nahi hai to free bana lein)
2. Upar right mein **"+" → "New repository"** dabayein
3. Repository name: `bbd-tools` likhein → **"Create repository"** dabayein
4. Naye khule page mein, **"uploading an existing file"** link pe click karein
5. Is poore `bbd-tools` folder (jo neeche diya hai) ke **sabhi files aur folders drag-and-drop** kar dein upload box mein
6. Neeche **"Commit changes"** button dabayein

Bas — aapka code ab GitHub par hai।

*(Agar aap laptop pe ho aur `git` command use karna jaante hain, to standard `git init`, `git add .`, `git commit`, `git push` bhi kar sakte hain — dono tarike se same result milega।)*

---

## ▲ Step 3 — Vercel Se Connect Karein (Auto-Deploy Ke Liye)

1. **vercel.com** pe jaake **"Sign Up"** → **"Continue with GitHub"** choose karein (isse aapka GitHub account connect ho jaayega)
2. Login hone ke baad, **"Add New..." → "Project"** dabayein
3. Apna `bbd-tools` repository dhoondh kar **"Import"** dabayein
4. Settings mein kuch change karne ki zaroorat nahi — seedha **"Deploy"** dabayein
5. 30-60 second mein aapko ek live link mil jaayega (jaisa `bbd-tools.vercel.app`)

**Sabse achhi baat:** Ab jab bhi aap GitHub pe koi file update/replace karenge (jaise placeholder ko apni real file se badlenge), **Vercel automatically 30 second mein naya version live kar dega** — dobara deploy karne ki zaroorat nahi।

---

## 🌐 Step 4 — Apna Custom Domain Jodein (Optional Lekin Recommended)

1. Vercel Dashboard mein apne project ke andar **"Settings" → "Domains"** mein jaayein
2. `tools.buildbasedigitally.com` type karke **"Add"** dabayein
3. Vercel aapko ek **DNS record** dikhayega (kuch is tarah: Type `CNAME`, Name `tools`, Value `cname.vercel-dns.com`)
4. Jahan se aapne `buildbasedigitally.com` domain liya hai (GoDaddy, Namecheap, Hostinger, etc.), wahan **DNS Settings** mein jaake yeh exact record add kar dein
5. 10-30 minute mein `tools.buildbasedigitally.com` live ho jaayega

---

## ✅ Final Result

| Tool | Link |
|---|---|
| Dashboard | `tools.buildbasedigitally.com` |
| Package Selector | `tools.buildbasedigitally.com/package-selector` |
| Onboarding Form | `tools.buildbasedigitally.com/onboarding-form` |
| Prompt Generator | `tools.buildbasedigitally.com/prompt-generator` |
| Checklist | `tools.buildbasedigitally.com/checklist` |

Ek hi link yaad rakhein (`tools.buildbasedigitally.com`), aur wahan se sabhi tools tak pahunch sakte hain।

---

## 🔄 Future Mein Naya Tool Add Karna Ho To

1. Ek naya folder banayein (jaise `naya-tool/`)
2. Uske andar `index.html` daalein
3. `index.html` (root wale Dashboard) mein ek naya card add kar dein us tool ke link ke saath
4. GitHub pe push/upload karein — Vercel automatically naya version deploy kar dega
