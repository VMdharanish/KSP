# KAVACH AI — Explainable Crime Intelligence Copilot

> **Karnataka State Police (KSP) Hackathon-Ready Decision-Support Application**  
> Positioned strictly as an explainable decision-support copilot for authorized police investigators and crime analysts.

---

## 🌟 Key Features

1. **Multilingual Natural Language Assistant**:
   - Supports queries in English, native Kannada script, and **Romanized Kannada** typed through an English keyboard (e.g., *"Mysuru alli kaleda tingalu kallatana casegalu torisi"*).
   - Displays clear translation confirmation banners (*"I understood your request as: ..."*).
2. **Prompt Completeness & Interactive Clarification**:
   - Detects incomplete prompts (e.g., *"Show theft cases"*) and provides selectable district & date period chips.
   - Disambiguates names (e.g., *"Find Ramesh"*) with candidate selector.
3. **Strict Read-Only Security Guard**:
   - AST/Regex engine enforces that database queries allow **`SELECT` and `WITH` only**.
   - Blocks `DROP`, `DELETE`, `INSERT`, `UPDATE`, `ALTER` and SQL injection attempts.
4. **Active Investigation FIR Workspace**:
   - Detailed FIR master view, chronological event timeline generator, and Cytoscape.js accused-case relationship visualizer with source table evidence inspection.
5. **Crime-Scene Image Assistant**:
   - Cryptographic **SHA-256 hash generation** on upload.
   - Categorized visual observations (*Clearly Visible*, *Possible Observation*, *Unclear*, *Requires Forensic Review*) with officer confirmation buttons.
6. **Crime Analytics & Leaflet Map**:
   - ECharts macro trends and Leaflet geographic map plotting FIR coordinates with missing location quality warnings.
7. **Structured PDF Report Generator**:
   - Downloads court-ready investigation briefs generated with jsPDF, featuring synthetic data disclaimers and human verification footers.
8. **Immutable Security Audit Logging**:
   - Tracks sensitive queries, role authorizations, image uploads, and report exports for administrator inspection.

---

## 🔐 Demo Credentials

| Role | Email ID | Password | Name & Jurisdiction |
| :--- | :--- | :--- | :--- |
| **Investigator** | `investigator@kavach.demo` | `Demo@123` | Inspector Vijay Kumar (Bengaluru City) |
| **Analyst** | `analyst@kavach.demo` | `Demo@123` | Crime Analyst Anita Rao (Mysuru) |
| **Admin** | `admin@kavach.demo` | `Demo@123` | System Admin SP Office |

---

## 💻 Tech Stack

- **Frontend**: React 18, TypeScript, Vite, Tailwind CSS, React Router, Lucide React icons
- **Visualizations**: ECharts (`echarts-for-react`), Cytoscape.js, Leaflet + OpenStreetMap (`react-leaflet`), jsPDF
- **Backend**: Node.js, Express (local adapter), Modular Zoho Catalyst Functions
- **Database Engine**: SQLite with WebAssembly (`sql.js`), strict DDL following official KSP schema
- **Validation**: Zod schema registry

---

## 🚀 Quick-Start Instructions (Local Development)

### 1. Install Dependencies
```bash
npm install
cd client && npm install && cd ..
```

### 2. Seed Synthetic KSP Database (50 FIR Records)
```bash
cmd /c npx ts-node database/seed.ts
```

### 3. Run Development Server
```bash
npm run dev
```
- Local Backend API: `http://localhost:5000`
- Vite Client App: `http://localhost:3000`

---

## 🧪 Run Automated Tests
```bash
cmd /c npx ts-node tests/run-all.ts
```

---

## 📋 Zoho Catalyst Deployment

See detailed instructions in [docs/catalyst-deployment.md](file:///e:/KSP%20hackathon/docs/catalyst-deployment.md).
```bash
npm --prefix client run build
zcatalyst deploy
```

---

## 📜 Disclaimer
This prototype uses synthetic demonstration records structured according to the supplied KSP FIR database schema. KAVACH AI is a decision-support system and does not replace official police investigation procedures.
