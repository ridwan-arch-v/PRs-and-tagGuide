### **Langkah-langkah untuk Update dengan Commit, PR, dan Tag**

### 1. **Buat Branch Baru**
Setiap kali Anda ingin membuat pembaruan, buatlah branch baru untuk mengisolasi perubahan yang akan Anda buat. Ini adalah praktik yang baik karena memungkinkan Anda untuk mengelola perubahan dengan lebih terorganisir.

```bash
git checkout -b nama-branch
```

Contoh: Jika Anda ingin menambahkan fitur baru, Anda bisa membuat branch dengan nama `add-feature`.

```bash
git checkout -b add-feature
```

### 2. **Lakukan Perubahan dan Commit**
Setelah membuat branch baru, lakukan perubahan pada file yang diperlukan. Setelah selesai melakukan perubahan, tambahkan file ke staging area dan commit perubahan tersebut.

```bash
git add .
git commit -m "Deskripsi tentang perubahan yang dilakukan"
```

Contoh:
```bash
git commit -m "Menambahkan fitur pencarian pada aplikasi"
```

### 3. **Buat Tag**
Setelah Anda melakukan commit dan siap untuk menyimpan versi pembaruan tersebut, buat tag dengan nama yang sesuai. Biasanya, tag ini akan digunakan untuk menandai rilis atau pembaruan besar.

Tag dapat dinamakan sesuai dengan versi atau dengan nama branch, agar mudah diingat. Misalnya, jika Anda membuat branch `add-feature`, Anda bisa memberi tag yang sama dengan nama branch.

```bash
git tag -a add-feature -m "Tag untuk fitur pencarian"
```

**Penjelasan**:
- `-a` berarti Anda membuat tag dengan anotasi (yang memungkinkan Anda menambahkan pesan ke tag tersebut).
- `-m` diikuti dengan pesan tag yang menjelaskan fitur atau pembaruan.

### 4. **Push Branch dan Tag ke Remote**
Sekarang, Anda perlu mengirimkan perubahan yang sudah Anda buat ke repository remote di GitHub atau GitLab. Gunakan perintah `push` untuk mengirimkan **branch** dan **tag**.

Untuk push **branch**:
```bash
git push origin add-feature
```

Untuk push **tag**:
```bash
git push origin add-feature
```

Jika Anda ingin mengirimkan **semua tag** sekaligus, gunakan perintah:
```bash
git push --tags
```

### 5. **Buat Pull Request (PR)**
Setelah Anda melakukan push branch ke remote repository, Anda bisa membuat **pull request (PR)** di GitHub atau GitLab untuk menggabungkan perubahan yang ada di branch tersebut ke branch utama (misalnya `main` atau `master`).

Berikut langkah-langkah membuat PR di GitHub:
1. Buka repository Anda di GitHub.
2. Klik tab **Pull Requests**.
3. Klik tombol **New Pull Request**.
4. Pilih branch `add-feature` yang Anda buat dan pilih **base branch** (biasanya `main` atau `master`).
5. Tulis deskripsi tentang perubahan yang Anda buat dalam pull request, misalnya "Menambahkan fitur pencarian".
6. Klik **Create Pull Request** untuk mengajukan PR.

### 6. **Review dan Merge Pull Request**
Setelah PR diajukan, Anda atau orang lain yang memiliki akses ke repository bisa melakukan review perubahan yang diajukan. Jika semuanya sudah sesuai, merge PR tersebut untuk menggabungkan perubahan ke branch utama.

Setelah **merge** PR selesai, Anda bisa menghapus branch yang sudah tidak diperlukan lagi, baik di lokal maupun di remote.

Untuk menghapus branch di remote:
```bash
git push origin --delete add-feature
```

Dan di lokal:
```bash
git branch -d add-feature
```

---

### **Contoh Lengkap dari Proses:**

Misalnya, Anda ingin memperbarui repository dengan menambahkan fitur baru, dan ingin menggunakan tag serta pull request. Berikut adalah contoh alur kerjanya:

1. **Buat Branch Baru**:
   ```bash
   git checkout -b add-search-feature
   ```

2. **Lakukan Perubahan dan Commit**:
   Misalnya, Anda menambahkan fitur pencarian di aplikasi. Lakukan perubahan pada file dan commit:
   ```bash
   git add .
   git commit -m "Menambahkan fitur pencarian di aplikasi"
   ```

3. **Buat Tag**:
   Anda dapat menandai pembaruan dengan tag yang sesuai. Nama tag ini bisa mengikuti nama branch atau versi.
   ```bash
   git tag -a add-search-feature -m "Tag untuk fitur pencarian"
   ```

4. **Push Branch dan Tag ke Remote**:
   Kirim perubahan dan tag ke remote repository:
   ```bash
   git push origin add-search-feature
   git push origin add-search-feature
   ```

5. **Buat Pull Request**:
   - Buka GitHub atau GitLab, lalu buat pull request dari `add-search-feature` ke `main`.
   - Tambahkan deskripsi yang jelas mengenai perubahan yang Anda buat.
   - Klik **Create Pull Request**.

6. **Review dan Merge PR**:
   Setelah PR diperiksa dan diterima, merge PR ke branch utama (`main`). Setelah itu, hapus branch yang tidak diperlukan.

7. **Hapus Branch yang Sudah Tidak Diperlukan**:
   - Hapus branch di remote:
     ```bash
     git push origin --delete add-search-feature
     ```

   - Hapus branch di lokal:
     ```bash
     git branch -d add-search-feature
     ```

---

### **Rangkuman:**
1. **Buat branch baru** untuk setiap perubahan.
2. **Lakukan perubahan**, commit, dan beri deskripsi yang jelas.
3. **Buat tag** dengan nama yang sama dengan nama branch atau versi tertentu.
4. **Push branch dan tag** ke remote repository.
5. **Buat Pull Request (PR)** untuk menggabungkan perubahan ke branch utama.
6. **Review dan merge PR**, lalu hapus branch yang sudah tidak diperlukan.

Dengan mengikuti langkah-langkah ini, Anda bisa memastikan setiap update di repository terorganisir dengan baik dan mudah dilacak melalui tag dan pull request.