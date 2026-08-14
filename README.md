# UNBUILT — README

> "Someone imagined it. Now someone can build it."

UNBUILT ek single-file website hai (`unbuilt-v4.html`) jahan log apne unfinished ideas post karte hain, aur builders un ideas ko dhoondh kar real projects me badalte hain. Ye document har feature ko section-wise explain karta hai.

---

## 1. Hero — "Idea Universe"

- Page open hote hi headline aur CTA buttons staggered animation ke saath fade-in hote hain (ek-ek karke, top se neeche).
- Background me ek animated **canvas particle system** hai — har particle ek idea ko represent karta hai. Mouse hover karne par nearby particle highlight hota hai aur uska naam tooltip me dikhta hai; click karne se us idea ka detail modal khulta hai.
- Do main CTA: **"I Have an Idea"** (idea publish karne ka wizard) aur **"I Need Something to Build"** (requirement-based idea matcher).
- Hero search bar — seedha keyword se ideas search karne ke liye.

## 2. Ideas / Discovery Grid

- Sabhi unbuilt ideas card-format me dikhte hain, filter tabs ke saath (jaise Trending, Newest, etc.).
- Har card me: problem statement, status badge (UNBUILT/CLAIMED/BUILDING/BUILT), builders count, aur quick actions.
- Cards scroll-me-aane-par fade-up animation ke saath reveal hote hain (staggered — ek ke baad ek).
- Hover karne par card halka sa upar uthta hai aur gold glow border dikhta hai.

## 3. Idea Detail Modal

Kisi bhi card pe click karne se poora idea detail modal khulta hai:

- **Status Track** — UNBUILT → CLAIMED → BUILDING → BUILT ka visual progress bar. Active stage ka dot dheere-dheere pulse (glow) karta rehta hai.
- **The Problem / Who Has This Problem / The Idea / Why It Matters / Creator's Vision** — poori idea ki story.
- **Required Skills & Possible Technologies** — tags ke roop me.
- **Idea DNA** — ek radar jaisa breakdown (creativity, feasibility, impact, etc.) progress-bars ke through.
- **Buildability Score** — 0–100% ka score jo batata hai idea kitni realistically buildable hai, ek chhoti si explanatory note ke saath.
- **MVP Cutter** — idea ko "Must Have / Nice to Have / Later" me automatically split karta hai, taaki pehla version chhota rakha ja sake.
- **Idea Evolution** — agar idea kisi aur idea ka remix hai (ya usse remix hui hai), to ek chain diagram dikhata hai.
- **Developer Rating AI (Build Score)** — jab idea BUILT ho chuki ho, to originality, problem-solving, technical depth, UX, execution, aur documentation par ek AI-style verdict aur score milta hai, saath me "Next Level" suggestions (95+ score tak pahunchne ke liye).
- Modal ab poori tarah **scrollable** hai (pehle ye bug tha, ab fix ho chuka hai).

### Actions inside the modal
- **"I Want to Build This"** — Now / This Week / Someday chunne ka intent menu khulta hai.
- **Claim Celebration** 🎉 — jab pehli baar koi idea claim hoti hai (UNBUILT → CLAIMED), ek celebratory gold-glow toast aur confetti burst animation dikhता hai.
- **Remix** — idea ka apna version bana sakte ho, jo original se linked rehta hai.
- **Save** — idea ko apne workspace me save karna.
- **Share** — idea share karna.

## 4. Shipped Projects

- Jo ideas actually BUILT ho chuki hain, unki ek alag list — origin idea aur usse jude sabhi contributors ke saath.

## 5. Build Together

- Wo ideas jo abhi bhi collaborators dhoondh rahi hain. Log bata sakte hain ki wo kya contribute kar sakte hain (skills/time), aur creator har offer ko review karta hai.

## 6. The Wall

- Ek casual, unpolished space — chhote unfinished thoughts post karne ke liye ("I wish there was a way to…", "Someone should build…" jaise prompts ke saath). Yahan se koi thought baad me structured idea me convert ho sakta hai.

## 7. Idea Graveyard

- Abandoned ideas ka collection — har idea ke saath ye likha hota hai ki wo kyun ruki. **"Revive This Idea"** button se koi bhi purani idea wapas UNBUILT state me la sakte ho.

## 8. My Workspace

- Personal dashboard: apni imagined/saved/built ideas, stats (ideas imagined, projects built, remixed, collaborations), aur tabs ke through alag-alag categories dekhna.

## 9. HAWKSTRANGE — AI Idea Assistant

- Ek floating chat button (bottom-right) jo hamesha screen par fixed rehta hai (pehle ye bug ki wajah se scroll ke saath bhatak jaata tha — ab fixed hai).
- Do wizard flows chalata hai:
  - **"I Have an Idea"** — raw thought ko structured idea page me convert karta hai.
  - **"I Need an Idea"** — tumhari skills, time, aur difficulty preference poochkar matching ideas suggest karta hai.
- Notifications panel bhi isi se juda hai (naye offers, claims, etc. ka update).

## 10. Design & Animation System

- **Dark, cinematic theme** — deep black background, soft gold accent, serif display font (Fraunces) + clean sans body font (Inter).
- **Scroll-reveal animations** — cards aur sections scroll me aane par smoothly fade-up hote hain.
- **Hero load-in sequence** — headline, CTA, search — sab staggered timing se andar aate hain.
- **Micro-interactions** — button press par halka scale-down, card hover par lift + glow.
- **Reduced-motion support** — agar user ke system me "reduce motion" on hai, to saari animations automatically off ho jaati hain (accessibility).

## 11. Bugs Fixed in This Version

| Issue | Root Cause | Fix |
|---|---|---|
| Modals/pages scroll nahi ho rahe the | Ek CSS rule sabhi direct body-children ko `position:relative` force kar raha tha, jisse modals ka `position:fixed` toot raha tha | Rule ko sirf `main` aur `footer` tak scope kiya |
| HAWKSTRANGE button/panel aur toast notifications scroll ke saath galat jagah chale jaate the | Same CSS rule se affected | Same fix se resolve |
| Claim karne par koi celebration nahi tha | Feature missing tha | Celebratory toast + confetti animation add kiya |

---

**File:** `unbuilt-v4.html` — single self-contained HTML file, koi build step nahi chahiye, seedha browser me kholo.
