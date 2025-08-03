 Multi Blockchain Wallet Scanner & Token Manager

=========================================================
📌 Deskripsi Singkat:
Script ini digunakan untuk:
- Memindai saldo token (EVM, Solana, Tron)
- Mengirim token dari wallet dengan saldo
- Membuat wallet baru (mnemonic atau private key)
- Mengecek koneksi RPC jaringan
- Mengelola dan memvalidasi mnemonic
- Support token EVM (ERC20), SPL (Solana), TRC20 (Tron)

=========================================================
📦 Ketergantungan / Requirements:

Instal semua dependensi dengan perintah:

pip install -r requirements.txt

Jika tidak punya file requirements.txt, install manual:

pip install -U web3 tronpy mnemonic bip44 colorama pyfiglet requests solana

⚠️ PENTING UNTUK SOLANA:
Script ini tidak support `solana-py` versi >= 0.3.x

WAJIB install versi 0.25.0:

pip uninstall solana -y
pip install solana==0.25.0

=========================================================
🔑 API KEY yang dibutuhkan:

1. API Alchemy (EVM RPC): [https://www.alchemy.com/](https://www.alchemy.com/)
2. API Helius (Solana SPL token): [https://www.helius.xyz/](https://www.helius.xyz/)
3. TronGrid API Key (opsional): [https://www.trongrid.io/](https://www.trongrid.io/)

API key diset manual di awal script:
- `HELIUS_API_KEY = ""`
- `TRONGRID_API_KEY = ""`

Silakan isi manual dengan API key milikmu.

=========================================================
🗂 File dan Struktur Penting:

- `phrases.txt` : Daftar mnemonic EVM
- `privatekeyevmgarapan.txt` : Daftar Private Key EVM
- `privatekeysol.txt` : Daftar Private Key Solana
- `privatekeytron.txt` : Daftar Private Key Tron
- `alamat_evm.txt` / `alamat_solana.txt` / `alamat_tron.txt` : daftar alamat publik untuk scan saldo
- `wallet_berisi_*.txt` : hasil scan saldo wallet
- `invalid_mnemonics.txt` : log mnemonic tidak valid
- `hasil_scan_by_address.txt` : hasil scan berdasarkan public address

=========================================================
▶️ Cara Menjalankan:

python namascript.py

Ikuti menu interaktif untuk memilih fitur.

=========================================================
📌 Catatan Tambahan:
- Semua transaksi blockchain akan ditandatangani otomatis menggunakan private key.
- Gunakan hanya untuk tujuan edukasi dan riset wallet pribadi.
- Jangan gunakan untuk aktivitas ilegal.
