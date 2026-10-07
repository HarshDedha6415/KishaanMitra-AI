# 🌾 KisanMitra AI
> **Grow Smarter. Protect Better. Sell Profitably.**

KisanMitra AI is an end-to-end, AI-driven agricultural decision-support ecosystem built for Indian farmers. Rather than presenting disjointed raw metrics, it synthesizes agro-climatic conditions, pathology imagery, dynamic commodity price trends, and logistics costs into a single prescriptive loop: **What to sow, how to protect, and precisely where and when to sell for peak net profit.**

---

## 1. Problem Statement

### The Problem
Indian farmers manage high biological and financial risk under severe decision uncertainty across every stage of the crop lifecycle:
* **Guesswork in Crop Selection:** Planting decisions depend largely on historical habit rather than soil composition, dynamic water tables, and seasonal market price forecasts.
* **Delayed Disease Diagnosis:** Visual leaf infections are diagnosed too late or misidentified, leading to excessive chemical expenditures or devastating crop loss.
* **The "Highest Price" Fallacy:** Farmers transport produce toward mandis displaying the highest headline price per quintal, only to discover that freight rates, transit shrinkage, and loading fees erase their net margins.
* **Data Fragmentation:** Critical insights—weather forecasts, Agmarknet feeds, and pathological treatments—are siloed across disjointed government portals and static dashboards.

The core challenge is not a lack of agricultural data.  
The core challenge is converting fragmented numbers into immediate, actionable decisions.

### Who Experiences This Problem?
* **Small and Marginal Farmers:** Producers with sub-2-hectare landholdings who cannot afford crop failures or unoptimized logistics expenses.
* **Medium-Scale Agriculturalists:** Multi-crop operators seeking to optimize seasonal timing and input overheads.
* **Farmer Producer Organizations (FPOs):** Collectives aggregating regional tonnage needing coordinated dispatch and market routing.
* **Rural Extension Workers & Agronomists:** Field advisors requiring fast, verified diagnostic benchmarks on-site.

### Why Is It a Problem? (The Breaking Loop)
Without unified decision support, the farming lifecycle breaks down:
## 1. The Core Problem

Kheti me sabse bada issue information ki kami nahi hai, balki fragmented information ki wajah se galat decision lena hai:

* **Andaze se fasal chunna:** Log purani aadat ya padosi ko dekh kar fasal bo dete hain, bina yeh jane ki unki mitti, aane wale mausam aur market demand me kya fit baithega.
* **Bimari pehchanne me deri:** Poda kharab hone lagta hai tab tak local dealer ke pass jaate hain, jahan aksar mehngi aur galat dawaiyan bech di jaati hain.
* **Mandi ka dhokha:** Zyadatar kisan us mandi me chale jaate hain jahan rate ₹100 zyada dikhta hai, par 50 km dur tractor ka diesel aur bhada katne ke baad hath me kam paise bachte hain.
* **10 alag jagah bhatakna:** Mausam ke liye alag app, mandi bhav ke liye alag portal, aur dawai ke liye kisi aur par depend hona padta hai.

### Kispar Asar Padta Hai?
* **Chote aur normal kisan:** Jinke paas risk lene ka margin zero hota hai.
* **FPOs (Farmer Producer Groups):** Jinko bulk me produce bechne ke liye smart routing chahiye hoti hai.
* **Field workers:** Jo gaon-gaon jakar sahi salah dena chahte hain.

### The Real Cycle (Jo ground reality hai)

Nayi Fasal Ka Plan
↓
Bina Data Ke Crop Selection
↓
Achanak Mausam Kharab / Keeda Lagna
↓
Mehnga Chemical Spray (Kharcha Badha)
↓
Pass/Dur Ki Mandi Me Bina Math Kiye Produce Bechna
↓
Diesel & Middleman Ke Baad Loss / Kam Munafa

---

## 2. Existing Apps vs KisanMitra AI

| Existing Apps | Ground Reality / Problem | KisanMitra Approach |
|---|---|---|
| **Agmarknet / e-NAM** | Sirf mandi rate batate hain. | Distance aur freight cost ghata kar **Net Pocket Profit** batata hai. |
| **Normal Weather Apps** | "70% rain expected" bolkar chhod dete hain. | Farming action batata hai: *"Aaj pani mat lagao, 2 din me barish hogi."* |
| **Plant Scanning Apps** | Complex scientific naam dete hain. | Desi ilaj + chemical dono batata hai, sath me treatment ka estimated kharcha bhi. |

---

## 3. Hamara Solution Kaise Kaam Karta Hai?

KisanMitra AI sabhi inputs ko combine karta hai aur ek line ka practical decision deta hai:


Farm Details (Mitti, Pani)  +  Live Weather  +  Mandi Rates & Freight
│
▼
[ KisanMitra Decision Core ]
│
┌───────────────────┼───────────────────┐
▼                   ▼                   ▼
Sahi Fasal Chuno     Patte Ki Bimari      Best Mandi & Timing
(Kam kharch, better) (Pehle din pakdo)   (Jahan actual bachat ho)

### Ek Simple Example:
* **Normal App bolega:** "Mandi B me ₹2,450 ka rate hai (40 km dur), Mandi A me ₹2,200 (15 km dur)."
* **KisanMitra AI batayega:** *"Mandi B jao. ₹4,000 transport kaatne ke baad bhi aapko Mandi A se ₹2,500 zyada bachenge."*

---

## 4. Main Features

1. **Smart Crop Advisory:** Aapke khet ki mitti, paani aur season ke hisaab se aisi faslein batata hai jisme input cost kam aur expected market return behtar ho.
2. **Action-First Weather Alerts:** Weather data ko real farming rules me badalna (jaise barish aane se pehle spray delay karne ka alert).
3. **Crop Doctor (Photo Scanner):** Poudhe ke patte ki photo click karo. Model bimari pehchanta hai, risk level batata hai aur turant kya karna hai wo batata hai.
4. **Mandi Net-Profit Calculator:** Sirf price nahi, balki `(Mandi Bhav × Wazan) - Gadi Ka Bhada - Mandi Kharcha = Asli Kamai` calculate karke best mandi suggest karta hai.
5. **Sell Now vs Wait:** Pichle trends aur crop kitne din tik sakti hai uske base par practical salah: *"Ruko ya turant becho."*
6. **Voice Support (Hindi / English):** Kisan type karne ke bajaye bol kar seedhe sawal pooch sake: *"Kya abhi gehun bechna sahi hai?"*

---

## 5. Under The Hood (Architecture & Logic)


KISAN (Voice / Photo / Input)
│
▼
React + Tailwind Frontend
│
▼ (API Calls)
FastAPI (Python Backend)
│
┌──────────────────────────────┼──────────────────────────────┐
▼                              ▼                              ▼
Weather Data Feed              Custom ML Models             Live Market Feeds
(OpenWeather)               (Vision + Classifiers)          (e-NAM / Local rates)
│
▼
Real Profit Math Engine
│
▼
Actionable Result Screen Par

### Modules:
* **Vision Pipeline:** MobileNet / CNN based lightweight model jo mobile camera se li gayi low-res leaf images par bhi reliably diagnose karta hai.
* **Recommendation Model:** Soil parameters (NPK, pH), paani aur season ko map karke suitable crops filter karta hai.
* **Profit Route Logic:** Simple deterministic freight math jo distance-per-km diesel cost ko produce ke quantity ke saath calculate karta hai.

---

## 6. Tech Stack

* **Frontend:** React.js, Tailwind CSS (Mobile-first, simple UI jo dhoop me bhi clearly dikhe)
* **Backend:** Python, FastAPI (Fast response time aur easy ML integration)
* **Database:** PostgreSQL (User farms, crop history, aur rate logs save karne ke liye)
* **Machine Learning:** PyTorch, Scikit-learn (Image classification aur tabular prediction ke liye)
* **External APIs:** OpenWeather API, Agmarknet feeds
* **Voice:** Web Speech API (Hands-free field use ke liye)

---

## 7. Future Roadmap

* **Soil Sensors Integration:** Saste Bluetooth/IoT probes jo seedhe phone ko mitti ki nami bata sakein.
* **Satellite Greenery Index (NDVI):** Bade kheton ke liye satellite imagery se water stress detect karna.
* **Direct Buyer Connect:** FPO level par seedhe millers aur bulk buyers se link karna taaki beech ka margin bache.
* **More Regional Languages:** Punjabi, Marathi, aur Telugu voice support add karna.

---

