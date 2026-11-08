# Learnova — Educational Website

एक आधुनिक, मोबाइल-फ्रेंडली शैक्षिक वेबसाइट जो React, HTML, CSS और JavaScript से बनी है। इसमें Home, About, Courses और Contact सेक्शन, responsive navigation, Learnova favicon, और एक डेमो संपर्क फ़ॉर्म शामिल है। Database, login और payment इसमें शामिल नहीं हैं।

## ज़रूरतें

- Node.js 20.19+ या 22.12+ (Vite की वर्तमान ज़रूरत)
- npm

## स्थानीय कंप्यूटर पर चलाएँ

1. इस `learnova` फ़ोल्डर को अपने कंप्यूटर पर रखें और टर्मिनल में इसी फ़ोल्डर पर जाएँ।
2. निर्भरताएँ इंस्टॉल करें:

   ```bash
   npm install
   ```

3. विकास सर्वर शुरू करें:

   ```bash
   npm run dev
   ```

4. टर्मिनल में दिखाया गया स्थानीय पता (आमतौर पर `http://localhost:5173`) ब्राउज़र में खोलें।

प्रोडक्शन बिल्ड देखने के लिए `npm run build` चलाएँ। बने हुए `dist` फ़ोल्डर को स्थानीय रूप से देखने के लिए `npm run preview` चलाएँ।

## Vercel पर Deploy करें

### GitHub के ज़रिए

1. `learnova` फ़ोल्डर को GitHub repository में push करें।
2. [Vercel](https://vercel.com/) में **Add New → Project** चुनें और repository import करें।
3. Root Directory में `learnova` (या repository के अनुसार वेबसाइट का फ़ोल्डर) चुनें।
4. Framework Preset **Vite**, Build Command `npm run build`, और Output Directory `dist` रखें। Install Command `npm install` रहने दें।
5. **Deploy** चुनें। Vercel हर नए push पर फिर से deploy कर सकता है।

### Vercel CLI के ज़रिए

Vercel CLI इंस्टॉल करके वेबसाइट फ़ोल्डर से चलाएँ:

```bash
npm install -g vercel
vercel
```

Production deployment के लिए `vercel --prod` चलाएँ। संकेत मिलने पर Vercel में लॉगिन करें और prompts पूरे करें।

## फ़ोल्डर संरचना

```text
learnova/
├── index.html
├── package.json
├── vite.config.js
├── README.md
├── public/
│   └── favicon.svg
└── src/
    ├── App.jsx
    ├── main.jsx
    └── styles.css
```

संपर्क फ़ॉर्म अभी केवल फ्रंटएंड डेमो है; सबमिट करने पर यह साफ़ बताता है कि संदेश नहीं भेजा गया है। यह संदेश कहीं भेजता या सहेजता नहीं है। Hero फोटो Unsplash से लोड होती है और DM Sans तथा Manrope फ़ॉन्ट Google Fonts से आते हैं, इसलिए इन्हें लोड करने के लिए इंटरनेट कनेक्शन चाहिए। देवनागरी के लिए स्थानीय system-font fallback भी मौजूद है।
