## Mata Kuliah
Sebagai Proyek UAS: Bahasa Pemrograman | Universitas Pelita Bangsa.

## Proyek UAS

|Video YouTube: |https://youtu.be/Im0750EMZ4Y |
| --- | --- |

<p align="left">
  <img src="/ss/hasil.jpg" width="450">
</p>

    def show_product_list(products):
        # Menampilkan daftar produk beserta harganya
        print(" NO | NAMA BARANG     | HARGA ")
        for i, (product_name, price) in enumerate(products.items(), start=1):
            print(f" {i}  | {product_name:15} | {price} ")


    def add_to_cart(products, code, quantity):
        # Menghitung total harga barang yang akan ditambahkan ke keranjang
        prices = list(products.values())
        total_price = prices[code - 1] * quantity
        return total_price


    def main():
        # Daftar produk beserta harga
        products = {
            "Snack Coklat": 2000,
            "Minuman Soda": 3500,
            "Es Teh Manis": 2500,
            "Beng-Beng": 5000,
        }

        # Menampilkan daftar produk
        show_product_list(products)
        cart = []  # Inisialisasi keranjang belanja

        while True:
            try:
                # Input untuk memilih nomor barang
                code = int(input("\nMasukkan nomor barang: "))
                if code < 1 or code > len(products):
                    print("Nomor barang tidak valid. Silakan coba lagi.")
                    continue
            except ValueError:
                print("Masukkan nomor barang berupa angka.")
                continue

            # Input untuk jumlah barang yang akan dibeli
            quantity = int(input("Masukkan jumlah barang: "))

            # Menambahkan barang ke dalam keranjang
            total_price = add_to_cart(products, code, quantity)
            cart.append(total_price)

            tanya_input = input("\nIngin tambah barang lagi? [y/t]: ")
            if tanya_input.lower() != "y":
                break

        print("\n---------------------")
        print("Detail Pembelian:\n")

        # Menampilkan detail pembelian, termasuk nama barang dan total harga
        for i, total_price in enumerate(cart, start=1):
            product_name = list(products.keys())[i - 1]
            print(
                f"{product_name}: {total_price} Rupiah"
            )  # Menampilkan nama barang dan total harga

        if cart:
            print("---------------")
            total_pembelian = sum(cart)
            print(
                f"Total Pembelian: {total_pembelian} Rupiah\n"
            )  # Menampilkan total harga pembelian


    if __name__ == "__main__":
        main()

fungsi dan penjelasan sudah tertera pada ***#*** dan ***print*** diatas.

## Flowchart | Proyek UAS
<p align="left">
  <img src="/ss/flowchart.jpg" width="180">
</p>

flowchart ini menggunakan ***dictionary*** beserta ***[]*** agar lebih mudah menempatkan ***value***.
sehingga ***append*** dapat di-fungsikan dengan lebih mudah.

## Documentation
All associated resources. are licensed under the [MIT License](https://mit-license.org/).
