# Implementasi Binary Search Tree (BST)

Repositori ini berisi implementasi Binary Search Tree (BST) dalam Python. BST adalah struktur data fundamental dalam ilmu komputer yang memfasilitasi pencarian, penambahan, dan penghapusan item dengan cepat. Implementasi ini mencakup fungsionalitas untuk menyisipkan, menghapus, mencari, dan melakukan traversal in-order pada pohon.

## Kelas

### BSTNode

Kelas `BSTNode` merepresentasikan satu node dalam binary search tree. Setiap node berisi sebuah kunci (key), serta referensi ke anak kiri dan kanan, serta orang tuanya (parent).

#### Metode

- **`__init__(self, key)`**: Menginisialisasi sebuah node dengan kunci yang diberikan. Pointer ke anak kiri, kanan, dan orang tua diatur ke `None`.

- **`insert(self, node)`**: Menyisipkan node baru ke dalam subtree yang berakar pada node saat ini.

- **`inorder(self)`**: Melakukan traversal in-order pada subtree yang berakar pada node saat ini, mencetak kunci-kuncinya.

- **`replace_node_of_parent(self, new_node)`**: Menggantikan node saat ini dengan `new_node` dalam referensi orang tuanya.

- **`find_min(self)`**: Menemukan node dengan kunci minimum dalam subtree yang berakar pada node saat ini.

- **`remove(self)`**: Menghapus node saat ini dari pohon.

- **`search(self, key)`**: Mencari node dengan kunci yang diberikan dalam subtree yang berakar pada node saat ini.

### BSTree

Kelas `BSTree` merepresentasikan seluruh binary search tree.

#### Metode

- **`__init__(self)`**: Menginisialisasi binary search tree kosong.

- **`inorder(self)`**: Melakukan traversal in-order pada seluruh pohon, dimulai dari akar.

- **`add(self, key)`**: Menambahkan node dengan kunci yang diberikan ke dalam pohon.

- **`remove(self, key)`**: Menghapus node dengan kunci yang diberikan dari pohon.

- **`search(self, key)`**: Mencari node dengan kunci yang diberikan dalam pohon.

## Penggunaan

Untuk menggunakan implementasi BST ini, Anda dapat menjalankan skrip dan berinteraksi dengannya melalui antarmuka baris perintah sederhana. Operasi yang tersedia adalah menambahkan node, menghapus node, melakukan traversal in-order, dan keluar dari program.

### Contoh

```python
if __name__ == "__main__":
    bstree = BSTree()
    print("Menu (dengan asumsi tidak ada kunci duplikat)")
    print("add <key>")
    print("remove <key>")
    print("inorder")
    print("quit")

    while True:
        do = input("Apa yang ingin Anda lakukan? ").split()
        operation = do[0].strip().lower()
        if operation == "add":
            key = int(do[1])
            bstree.add(key)
        elif operation == "remove":
            key = int(do[1])
            bstree.remove(key)
        elif operation == "inorder":
            print("Traversal in-order: ", end="")
            bstree.inorder()
            print()
        elif operation == "quit":
            break
```

### Perintah

- **`add <key>`**: Menambahkan node dengan kunci yang ditentukan ke dalam BST.
- **`remove <key>`**: Menghapus node dengan kunci yang ditentukan dari BST.
- **`inorder`**: Mencetak kunci dari node-node dalam BST dalam traversal in-order.
- **`quit`**: Keluar dari program.

## Kontribusi

Jangan ragu untuk fork repositori ini dan melakukan modifikasi atau perbaikan. Pull request sangat diterima.

## Lisensi

Proyek ini dilisensikan di bawah Lisensi MIT. Lihat file (LICENSE) untuk detail lebih lanjut.

---

README ini memberikan gambaran umum tentang implementasi BST, termasuk deskripsi kelas, ringkasan metode, dan instruksi penggunaan. Ini diharapkan dapat membantu pengguna memahami cara menggunakan dan berinteraksi dengan kode BST yang disediakan.
