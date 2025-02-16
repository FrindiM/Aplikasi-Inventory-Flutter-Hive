# 📦 Inventory Barang Kantor dengan Flutter & Hive

Aplikasi sederhana untuk mengelola inventory barang kantor menggunakan Flutter dan Hive sebagai database lokal.

---

## 🚀 Fitur Utama
- Tambah, edit, dan hapus data barang.
- Penyimpanan lokal menggunakan Hive (NoSQL).
- Tampilan responsif dan user-friendly.

---

## 🛠️ Teknologi yang Digunakan
- **Flutter**: Framework UI untuk pengembangan aplikasi cross-platform.
- **Hive**: Database NoSQL yang ringan dan cepat.
- **Provider**: State management yang sederhana dan efisien.

---

## 📋 Instalasi

1️⃣ Clone repository ini:

```bash
git clone https://github.com/username/repository.git
```

2️⃣ Masuk ke direktori proyek:

```bash
cd nama_proyek
```

3️⃣ Install dependencies:

```bash
flutter pub get
```

4️⃣ Jalankan aplikasi:

```bash
flutter run
```

---

## 📂 Struktur Proyek

```
/lib
│
├── main.dart
├── models
│   └── item_model.dart
├── screens
│   ├── home_screen.dart
│   ├── add_item_screen.dart
├── widgets
│   └── item_tile.dart
├── hive
│   └── hive_boxes.dart
└── utils
    └── constants.dart
```

---

## 🗂️ Setup Hive

1️⃣ Inisialisasi Hive di `main.dart`:

```dart
void main() async {
  WidgetsFlutterBinding.ensureInitialized();
  await Hive.initFlutter();
  Hive.registerAdapter(ItemModelAdapter());
  runApp(MyApp());
}
```

2️⃣ Buat model Hive:

```dart
@HiveType(typeId: 0)
class ItemModel {
  @HiveField(0)
  String name;

  @HiveField(1)
  int quantity;

  @HiveField(2)
  String category;
}
```

---

## 🐞 Troubleshooting

Jika ada masalah saat menjalankan aplikasi:

```bash
flutter clean
flutter pub get
```

---


## 📄 Lisensi

Proyek ini menggunakan lisensi MIT. Silakan lihat file `LICENSE` untuk detail lebih lanjut.

---

✨ Selamat ngoding! Semoga aplikasi ini bermanfaat untuk pengelolaan barang kantor Anda! 🚀

