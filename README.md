

---

🎥 WebRTC Live Streaming Platform

Platform live streaming berbasis WebRTC dengan Firebase sebagai backend untuk autentikasi dan manajemen data. Project ini memungkinkan pengguna untuk menjadi streamer atau menonton live secara real-time langsung dari browser tanpa plugin tambahan.


---

🚀 Fitur Utama

🔴 Live Streaming Real-time menggunakan WebRTC

👥 Multi-user (1 streamer, banyak viewer)

🔐 Firebase Authentication (Login / Register)

📦 Firestore sebagai signaling server WebRTC

🖥️ Tanpa media server (peer-to-peer)

📱 Responsive Design (Desktop & Mobile)

🎨 Animasi UI menggunakan Animista CSS Animations



---

🛠️ Teknologi yang Digunakan

Frontend

HTML5

CSS3

JavaScript (ES Module)

WebRTC API


Backend / Cloud

Firebase Authentication

Firebase Firestore

Firebase Hosting (opsional)



---

📂 Struktur Folder

├── index.html        # Halaman utama (landing / login)
├── stream.html       # Halaman streamer
├── watch.html        # Halaman penonton
├── admin.html        # Halaman admin (opsional)
├── css/
│   └── style.css     # Styling & animasi
├── js/
│   ├── firebase.js   # Konfigurasi Firebase
│   ├── stream.js     # Logic WebRTC streamer
│   ├── watch.js      # Logic WebRTC viewer
│   └── auth.js       # Login & register
└── README.md


---

🔧 Cara Instalasi & Menjalankan

1️⃣ Clone Repository

git clone https://github.com/zakyarchh/webRTC
cd webRTC

2️⃣ Konfigurasi Firebase

Buat project di Firebase Console, lalu aktifkan:

Authentication (Email/Password)

Firestore Database


Masukkan konfigurasi Firebase ke file:

// firebase.js
import { initializeApp } from "https://www.gstatic.com/firebasejs/12.9.0/firebase-app.js";

const firebaseConfig = {
  apiKey: "API_KEY",
  authDomain: "PROJECT_ID.firebaseapp.com",
  projectId: "PROJECT_ID",
};

export const app = initializeApp(firebaseConfig);


---

3️⃣ Jalankan Project

> ⚠️ WebRTC tidak bisa berjalan via file://



Gunakan local server:

npx serve

atau

php -S localhost:8000

Buka di browser:

http://localhost:3000


---

🔄 Cara Kerja Singkat WebRTC

1. Streamer membuat room


2. Offer SDP disimpan di Firestore


3. Viewer mengambil offer & mengirim answer


4. ICE Candidate dipertukarkan via Firestore


5. Koneksi peer-to-peer terbentuk 🎉




---

⚠️ Catatan Penting

WebRTC P2P → tidak cocok untuk ribuan penonton

Untuk skala besar, disarankan:

Media Server (SFU seperti Janus / Mediasoup)


Firebase Storage tidak digunakan



---

📌 Roadmap (Rencana Fitur)

💬 Live chat

🎁 Sistem gift / token

📺 Rekaman live

🌍 Multi-language (ID / JP)

📢 Iklan otomatis untuk user gratis



---

🤝 Kontribusi

Pull request sangat diterima.
Silakan fork repository ini dan buat branch baru.


---

📄 Lisensi

MIT License
Bebas digunakan untuk belajar dan pengembangan.

