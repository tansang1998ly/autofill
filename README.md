<!DOCTYPE html>
<html lang="vi">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no">
    <title>AutoFill Studio Pro - autofill.com</title>
    <!-- Favicon / Biểu tượng trang web -->
    <link rel="icon" href="https://cdn-icons-png.flaticon.com/512/281/281760.png" type="image/x-icon">
    
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        html, body {
            width: 100%;
            height: 100%;
            overflow: hidden;
            background-color: #0f172a; /* Màu nền tối khớp với giao diện WebApp */
            font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, Helvetica, Arial, sans-serif;
        }
        .iframe-container {
            width: 100%;
            height: 100%;
            position: absolute;
            top: 0;
            left: 0;
            border: none;
        }
        iframe {
            width: 100%;
            height: 100%;
            border: none;
            display: block;
        }
        /* Hiệu ứng nạp trang trong lúc chờ Google Apps Script tải */
        .loading-screen {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background-color: #0f172a;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            color: #94a3b8;
            z-index: -1;
        }
        .spinner {
            width: 40px;
            height: 40px;
            border: 4px solid #1e293b;
            border-top: 4px solid #6366f1;
            border-radius: 50%;
            animation: spin 1s linear infinite;
            margin-bottom: 12px;
        }
        @keyframes spin {
            0% { transform: rotate(0deg); }
            100% { transform: rotate(360deg); }
        }
    </style>
</head>
<body>

    <!-- Màn hình chờ khi nạp app -->
    <div class="loading-screen">
        <div class="spinner"></div>
        <p style="font-size: 14px;">Đang tải AutoFill Studio Pro...</p>
    </div>

    <!-- Khung nhúng WebApp Google Apps Script -->
    <div class="iframe-container">
        <!-- 
            LƯU Ý quan trọng: 
            Thay đường dẫn bên dưới bằng LINK EXEC WEBAPP Google Apps Script của bạn.
        -->
        <iframe 
            src="https://script.google.com/macros/s/AKfycbyss_PLoa76ECOyeHJQbBenl7agt8kOqS-f31VT9rdijy5p0iP4-JTddVXZ9JUyF9yu_w/exec" 
            allow="downloads; clipboard-write" 
            sandbox="allow-forms allow-modals allow-popups allow-popups-to-escape-sandbox allow-same-origin allow-scripts">
        </iframe>
    </div>

</body>
</html>
