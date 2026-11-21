# Yunus Computer Studio Pro

বাংলা-ভিত্তিক, offline-first computer studio web app starter. GitHub + Netlify-তে deploy করা যাবে।

## চালু করা
1. ZIP extract করুন।
2. GitHub-এ নতুন repository তৈরি করে সব ফাইল root-এ upload করুন।
3. Netlify → Add new site → Import an existing project → GitHub repository নির্বাচন করুন।
4. Build command: `npm run build`, Publish directory: `dist`।
5. Deploy শেষে সাইট খুলে Chrome/Edge থেকে Install App করতে পারবেন।

লোকাল ডেভেলপমেন্ট: Node.js 20+ লাগবে; `npm install` তারপর `npm run dev`।

## এই সংস্করণে কাজ করে
- Dashboard, module navigation এবং online/offline indicator
- Photo Studio: ছবি আপলোড, preset/custom size, rotate, brightness, contrast, saturation, grayscale, JPEG/PNG download
- Photo print sheet: 4R/A4, কপি সংখ্যা, browser print dialog
- CV/Biodata builder: তথ্য লিখে print/save as PDF
- Poster/card maker: editable title/body/shape/background, image upload, PNG export
- Audio script studio: script editor ও browser speech preview (বাংলা voice availability আপনার device/browser-এর উপর নির্ভরশীল)
- QR code: QR তৈরি করার বদলে এখানে এখন text-based print utility placeholder রাখা হয়েছে; QR algorithm integration পরবর্তী ধাপ
- Customer/job register: local browser storage, add/search/status update/delete
- Income/expense ledger: local browser storage, totals
- JSON backup/restore এবং CSV export
- PWA app-shell caching

## গুরুত্বপূর্ণ সীমাবদ্ধতা
- Browser print dialog ছাড়া নীরবে printer-এ print করা যায় না।
- SpeechSynthesis preview-এর অডিওকে নির্ভরযোগ্য MP3/WAV ফাইলে export করা browser API দিয়ে সম্ভব নয়।
- Background removal, face recognition, AI upscaling, OCR, Bengali neural TTS, DOCX↔PDF/Excel-এর faithful conversion এবং advanced PDF merge/split-এর জন্য আলাদা open-source model/library বা backend integration প্রয়োজন। এই সংস্করণ সেগুলো সম্পন্ন হয়েছে বলে দাবি করে না।
- ডেটা এই browser/device-এ থাকে। অন্য কম্পিউটারে দেখতে Backup থেকে JSON export করে Restore করতে হবে। একাধিক কম্পিউটারে live sync করতে database + authentication backend লাগবে।
- Offline প্রথমবার ব্যবহার করার আগে সাইট একবার online খুলে নিতে হবে।
