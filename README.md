<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no">
    <title>Pembayaran QRIS</title>
    <style>
        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            background-color: #f7f9fc;
            margin: 0;
            padding: 0;
            display: flex;
            justify-content: center;
            min-height: 100vh;
        }
        .main-container {
            width: 100%; /* Full lebar layar HP */
            max-width: 100%; 
            background-color: #ffffff;
            display: flex;
            flex-direction: column;
            min-height: 100vh;
        }

        /* Header - Full Width */
        .payment-header {
            padding: 20px;
            border-bottom: 1px solid #edf2f7;
        }
        .service-title {
            color: #1a202c;
            font-size: 16px;
            font-weight: 600;
            margin-bottom: 5px;
        }
        .price {
            color: #111111;
            font-size: 24px;
            font-weight: 700;
        }

        /* Detail Pembayaran */
        .payment-detail {
            padding: 15px 20px;
            background-color: #f8fafc;
            border-bottom: 1px solid #edf2f7;
        }
        .detail-label {
            color: #718096;
            font-size: 14px;
        }

        /* Area Utama QR Code - Dibuat Lebih Besar */
        .qr-section {
            padding: 40px 20px;
            text-align: center;
            display: flex;
            flex-direction: column;
            align-items: center;
            flex-grow: 1;
        }
        .qr-instruction-title {
            color: #111111;
            font-size: 18px;
            font-weight: 600;
            margin-bottom: 10px;
        }
        .qr-instruction-desc {
            color: #4a5568;
            font-size: 14px;
            margin-bottom: 30px;
            line-height: 1.5;
        }

        /* Container QR Code - Ukuran disesuaikan layar */
        .qr-code-container {
            width: 80vw; /* 80% dari lebar layar */
            height: 80vw;
            max-width: 320px;
            max-height: 320px;
            border-radius: 12px;
            padding: 15px;
            background: white;
            box-shadow: 0 4px 15px rgba(0,0,0,0.1);
            display: flex;
            justify-content: center;
            align-items: center;
            margin-bottom: 30px;
        }
        .qr-code-container img {
            width: 100%;
            height: 100%;
            display: block;
            object-fit: contain;
        }

        /* Tombol Simpan QR - Lebih Lebar */
        .download-button {
            display: flex;
            align-items: center;
            justify-content: center;
            width: 90%; /* Hampir full lebar layar */
            padding: 16px;
            background-color: #0045e0;
            color: white;
            border: none;
            border-radius: 10px;
            text-decoration: none;
            font-size: 16px;
            font-weight: 600;
            margin-bottom: 20px;
        }

        /* Status & Footer */
        .status-box {
            display: flex;
            align-items: center;
            width: 90%;
            padding: 12px 15px;
            background-color: #edf2f7;
            border-radius: 8px;
            font-size: 13px;
            color: #4a5568;
            margin-bottom: 20px;
            text-align: left;
        }
        .status-icon {
            min-width: 18px;
            height: 18px;
            background-color: #718096;
            color: white;
            border-radius: 50%;
            display: flex;
            justify-content: center;
            align-items: center;
            font-size: 11px;
            margin-right: 10px;
        }
    </style>
</head>
<body>

    <div class="main-container">
        <div class="payment-header">
            <div class="service-title">Weekly Diamond Pass</div>
            <div class="price">Rp. 27.000</div>
        </div>

        <div class="payment-detail">
            <div class="detail-label">Pembayaran melalui <b>QRIS</b></div>
        </div>

        <div class="qr-section">
            <div class="qr-instruction-title">Kode QR</div>
            <div class="qr-instruction-desc">Pindai atau unggah kode QR ini menggunakan aplikasi perbankan/dompet digital Anda.</div>

            <div class="qr-code-container">
                <img src="qris.png" alt="QR Code">
            </div>

            <a href="qris.png" download class="download-button">
                <svg width="18" height="18" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2.5" stroke-linecap="round" stroke-linejoin="round" style="margin-right: 8px;"><path d="M21 15v4a2 2 0 0 1-2 2H5a2 2 0 0 1-2-2v-4"></path><polyline points="7 10 12 15 17 10"></polyline><line x1="12" y1="15" x2="12" y2="3"></line></svg>
                Simpan Kode QR
            </a>

            <div class="status-box">
                <div class="status-icon">i</div>
                <div>Halaman ini akan diperbarui otomatis setelah pembayaran selesai.</div>
            </div>
        </div>
    </div>

</body>
</html>
