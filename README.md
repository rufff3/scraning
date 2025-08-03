
# 🛡️ Multi Blockchain Wallet Scanner & Token Manager

Script Python ini digunakan untuk:
- 🔍 **Memindai saldo token** di jaringan EVM (Ethereum, BSC, Polygon, dll), Solana, dan Tron
- 🚀 **Mengirim token** dari wallet yang memiliki saldo
- 🧩 **Membuat wallet baru** (mnemonic atau private key)
- 🌐 **Mengecek koneksi semua jaringan RPC**
- 🧹 **Memvalidasi dan membersihkan mnemonic**
- 📄 **Scan saldo berdasarkan public address**
- ✅ Support token:
  - EVM (ERC20)
  - Solana (SPL)
  - Tron (TRC20)

---

## 🛠️ Fitur Utama

✅ Scan saldo token EVM (custom token ERC20)  
✅ Scan saldo Solana (SOL & SPL Token)  
✅ Scan stablecoin Tron (USDT, USDC, TUSD)  
✅ Generate wallet baru  
✅ Kirim token secara otomatis  
✅ Deteksi alamat wallet dari private key

---

## 📂 Struktur File

| File                                   | Deskripsi                                    |
|----------------------------------------|----------------------------------------------|
| `phrases.txt`                          | Daftar mnemonic EVM                         |
| `privatekeyevmgarapan.txt`             | Daftar private key EVM                      |
| `privatekeytron.txt`                   | Daftar private key Tron                     |
| `privatekeysol.txt`                    | Daftar private key Solana                   |
| `alamat_evm.txt`                       | Daftar alamat EVM untuk scan saldo          |
| `alamat_solana.txt`                    | Daftar alamat Solana untuk scan saldo       |
| `alamat_tron.txt`                      | Daftar alamat Tron untuk scan saldo         |
| `wallet_berisi_*.txt`                  | Hasil scan saldo wallet                     |
| `invalid_mnemonics.txt`                | Mnemonic tidak valid                        |
| `hasil_scan_by_address.txt`            | Hasil scan berdasarkan alamat publik        |

---

## ⚠️ Dependencies & Instalasi

**WAJIB Python >= 3.8**

Install semua dependensi dengan:

```
pip install -r requirements.txt
```

Jika tidak punya `requirements.txt`, install manual:

```
pip install -U web3 tronpy mnemonic bip44 colorama pyfiglet requests
```

> 🟠 **PENTING UNTUK SOLANA:**
>
> Script ini **TIDAK support** `solana-py` versi 0.3.x.
>
> **WAJIB pakai versi 0.25.0:**

```
pip uninstall solana -y
pip install solana==0.25.0
```

---

## 🔑 Konfigurasi API Key

Script membutuhkan API Key berikut:

| Jaringan     | API Key                               | Link Daftar / Ambil Key                                     |
|--------------|---------------------------------------|------------------------------------------------------------|
| EVM          | Alchemy RPC API Key                  | https://www.alchemy.com/                                   |
| Solana       | Helius API Key                       | https://www.helius.xyz/                                    |
| Tron         | TronGrid API Key (Opsional)          | https://www.trongrid.io/                                   |

**Cara set:**
Buka script `addres.py`, cari variabel berikut, dan isi manual:

```
HELIUS_API_KEY = "MASUKKAN_API_KEY_HELIUS"
TRONGRID_API_KEY = "MASUKKAN_API_KEY_TRONGRID"
```

---

## ▶️ Cara Menjalankan

Jalankan script dengan:

```
python addres.py
```

Ikuti menu interaktif:

```
1. Scan Saldo Token
2. Kirim Token
3. Generate Wallet Baru
4. Cek Alamat Wallet
5. Scan Saldo Tron
6. Validasi Mnemonic
```

---

## ⚠️ Disclaimer

Script ini dibuat untuk **penelitian, edukasi, dan manajemen wallet pribadi**.  
**DILARANG** menggunakan untuk aktivitas ilegal.  
Penulis tidak bertanggung jawab atas penyalahgunaan.

---
