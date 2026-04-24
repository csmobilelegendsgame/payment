<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Pembayaran QRIS</title>
    <style>
        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            background-color: #f7f9fc;
            margin: 0;
            padding: 0;
            display: flex;
            justify-content: center;
            align-items: center;
            min-height: 100vh;
        }
        .main-container {
            width: 100%;
            max-width: 480px; /* Batasan lebar agar tidak terlalu lebar di PC */
            background-color: #ffffff;
            box-shadow: 0 4px 12px rgba(0,0,0,0.08);
            overflow: hidden;
            display: flex;
            flex-direction: column;
        }

        /* Bagian Atas / Header */
        .payment-header {
            padding: 16px 20px;
            border-bottom: 1px solid #edf2f7;
        }
        .service-title {
            color: #1a202c;
            font-size: 15px;
            font-weight: 600;
            margin-bottom: 4px;
        }
        .price {
            color: #111111;
            font-size: 20px;
            font-weight: 700;
        }

        /* Bagian Detail Pembayaran */
        .payment-detail {
            padding: 12px 20px;
            background-color: #f8fafc;
            border-bottom: 1px solid #edf2f7;
            display: flex;
            align-items: center;
        }
        .detail-label {
            color: #718096;
            font-size: 13px;
            margin-right: 8px;
        }
        .detail-value {
            display: flex;
            align-items: center;
        }
        .detail-value img {
            height: 14px; /* Atur tinggi logo QRIS di teks */
            margin-left: 4px;
        }

        /* Area Utama QR Code */
        .qr-section {
            padding: 30px 20px 20px;
            text-align: center;
            display: flex;
            flex-direction: column;
            align-items: center;
        }
        .qr-instruction-title {
            color: #111111;
            font-size: 16px;
            font-weight: 600;
            margin-bottom: 8px;
        }
        .qr-instruction-desc {
            color: #4a5568;
            font-size: 13px;
            margin-bottom: 24px;
            line-height: 1.4;
            max-width: 320px;
        }

        /* Container untuk QR Code */
        .qr-code-container {
            width: 200px;
            height: 200px;
            border-radius: 8px;
            padding: 10px;
            background: white;
            box-shadow: 0 2px 8px rgba(0,0,0,0.05);
            display: flex;
            justify-content: center;
            align-items: center;
            margin-bottom: 24px;
            overflow: hidden;
        }
        .qr-code-container img {
            max-width: 100%;
            max-height: 100%;
            display: block;
        }

        /* Tombol Simpan QR */
        .download-button {
            display: flex;
            align-items: center;
            justify-content: center;
            width: 100%;
            max-width: 280px;
            padding: 12px;
            background-color: #0045e0; /* Warna biru tombol */
            color: white;
            border: none;
            border-radius: 8px;
            text-decoration: none;
            font-size: 14px;
            font-weight: 600;
            cursor: pointer;
            transition: background-color 0.2s;
            margin-bottom: 16px;
        }
        .download-button:hover {
            background-color: #0037a3;
        }
        .download-button img {
            width: 16px;
            height: 16px;
            margin-right: 8px;
        }

        /* Status Pembayaran */
        .status-box {
            display: flex;
            align-items: center;
            width: 100%;
            max-width: 320px;
            padding: 10px 14px;
            background-color: #edf2f7;
            border-radius: 6px;
            font-size: 12px;
            color: #4a5568;
            margin-bottom: 12px;
        }
        .status-icon {
            width: 14px;
            height: 14px;
            background-color: #718096;
            color: white;
            border-radius: 50%;
            display: flex;
            justify-content: center;
            align-items: center;
            font-size: 10px;
            margin-right: 8px;
        }

        /* Footer */
        .footer-secure {
            display: flex;
            align-items: center;
            font-size: 12px;
            color: #a0aec0;
            margin-bottom: 30px;
        }
        .secure-icon {
            width: 12px;
            height: 12px;
            margin-right: 6px;
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
            <div class="detail-label">Pembayaran melalui</div>
            <div class="detail-value">
                <span>QRIS</span>
            </div>
        </div>

        <div class="qr-section">
            <div class="qr-instruction-title">Kode QR</div>
            <div class="qr-instruction-desc">Pindai atau unggah kode QR ini menggunakan aplikasi perbankan/dompet digital QRIS Anda untuk menyelesaikan pembayaran Anda.</div>

            <div class="qr-code-container">
                <img src="qris.png" alt="QR Code Pembayaran">
            </div>

            <a href="qris.png" download class="download-button">
                <svg width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2.5" stroke-linecap="round" stroke-linejoin="round" style="margin-right: 8px;"><path d="M21 15v4a2 2 0 0 1-2 2H5a2 2 0 0 1-2-2v-4"></path><polyline points="7 10 12 15 17 10"></polyline><line x1="12" y1="15" x2="12" y2="3"></line></svg>
                Simpan Kode QR
            </a>

            <div class="status-box">
                <div class="status-icon">i</div>
                <div>Halaman ini akan diperbarui setelah pembayaran selesai.</div>
            </div>

            <div class="footer-secure">
                <svg class="secure-icon" viewBox="0 0 24 24" fill="currentColor"><path d="M12 2C6.48 2 2 6.48 2 12s4.48 10 10 10 10-4.48 10-10S17.52 2 12 2zm1 15h-2v-2h2v2zm0-4h-2V7h2v6z"></path></svg>
                Secure Payment
            </div>
        </div>
    </div>

</body>
</html>
