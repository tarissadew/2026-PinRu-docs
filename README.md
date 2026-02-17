# System Architecture & Design - PinRu

Dokumentasi ini berisi rancangan teknis mengenai arsitektur sistem, skema database, dan alur kerja aplikasi PinRu yang telah diimplementasikan.

## 1. Entity Relationship Diagram (ERD)
Struktur data difokuskan pada sinkronisasi antara kapasitas ruangan dan status transaksi peminjaman.

### **Tabel Utama**
| Tabel | Deskripsi |
| :--- | :--- |
| `Rooms` | Menyimpan data aset ruangan, kapasitas total, dan lokasi. |
| `Bookings` | Menyimpan data transaksi peminjaman dengan status (Pending, Approved, Rejected). |
| `Users` | Menyimpan identitas pengguna dan peran (Admin/Customer). |

## 2. System Architecture
Sistem PinRu menggunakan arsitektur **Decoupled (Terpisah)** yang memungkinkan skalabilitas dan kemudahan pemeliharaan:

- **Frontend (Client Side)**: Dibangun menggunakan **React (Vite)**. Bertanggung jawab atas antarmuka pengguna, menangani state lokal, dan berkomunikasi dengan server melalui HTTP Client (Axios/Fetch).
- **Backend (Server Side)**: Dibangun menggunakan **ASP.NET Core 10**. Bertanggung jawab atas seluruh logika bisnis, validasi keamanan, dan pengelolaan data di database.
- **RESTful API**: Sebagai jembatan komunikasi antara Frontend dan Backend menggunakan format data JSON.
- **Database (Data Layer)**: Menggunakan **PostgreSQL** untuk penyimpanan data relasional yang persisten.

## 3. Technology Stack
- **Backend**: C# / ASP.NET Core 10 (Web API).
- **ORM**: Entity Framework Core.
- **Frontend**: React 18 (TypeScript) & Vite.
- **Styling**: Tailwind CSS & Lucide React.
- **Database**: PostgreSQL.

## 4. Core Business Logic
Aplikasi ini menerapkan beberapa logika kunci:
1. **Dynamic Capacity**: Sisa kuota ruangan dihitung secara real-time berdasarkan peminjaman yang berstatus `Approved`.
2. **Real-time Search**: Fitur pencarian instan untuk mempercepat akses informasi ruangan dan riwayat pinjaman.
3. **Role-based Access**: Pembedaan tampilan dan fungsi antara Admin (Monitoring & Verifikasi) dan Customer (Booking & Riwayat).

## 5. Workflows
- **Versioning**: Menggunakan Semantic Versioning (v1.0.0 Backend, v1.0.0 Frontend).
- **Git Branching**: Pengembangan dilakukan secara terpusat pada branch `main`.
- **Environment**: Pengembangan dilakukan di lingkungan lokal menggunakan VS Code.

---
*Terakhir diperbarui: 17 Februari 2026*