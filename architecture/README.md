# System Architecture & Design - PinRu

[cite_start]Bagian ini berisi dokumentasi teknis mengenai rancangan arsitektur sistem, skema database, dan alur kerja aplikasi PinRu.

## 1. Entity Relationship Diagram (ERD)
[cite_start]ERD menjelaskan struktur data dan hubungan antar tabel di dalam database, khususnya untuk modul CRUD Master Customer[cite: 173, 196].
> *Draf/Gambar ERD akan segera diunggah di sini.*

## 2. System Architecture
[cite_start]Penjelasan bagaimana komponen Backend (ASP.NET), Frontend (Web), dan Mobile (Flutter/Android) saling berkomunikasi melalui REST API [cite: 7, 182-186].
- [cite_start]**Backend**: Melayani logika bisnis dan akses database[cite: 230].
- [cite_start]**Frontend/Mobile**: Antarmuka pengguna untuk interaksi data[cite: 250, 251].

## 3. Technology Stack
- [cite_start]**Framework Backend**: ASP.NET Core[cite: 8, 229].
- [cite_start]**Database**: PostgreSQL / SQL Server[cite: 231].
- [cite_start]**Version Control**: Git & GitHub[cite: 3].
- [cite_start]**Versioning**: Semantic Versioning (SemVer)[cite: 121, 123].

## 4. Workflows
[cite_start]Alur kerja pengembangan menggunakan **Git Branching Strategy** (main, develop, feature/*)[cite: 70, 72, 222].