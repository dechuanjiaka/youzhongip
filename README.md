# youzhongip
youzhong ip 
<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>优众代理平台 - 专享注册通道</title>
    <style>
        /* 基础重置与字体设置 */
        * { box-sizing: border-box; margin: 0; padding: 0; }
        body {
            font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, "Helvetica Neue", Arial, sans-serif;
            background-color: #f2f5f9;
            color: #333;
            line-height: 1.6;
            display: flex;
            justify-content: center;
            align-items: center;
            min-height: 100vh;
            padding: 20px 10px;
        }
        /* 主卡片容器 */
        .card {
            background: #ffffff;
            width: 100%;
            max-width: 480px;
            border-radius: 16px;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.08);
            padding: 30px 20px;
            text-align: center;
        }
        /* 顶部图标与标题 */
        .icon {
            font-size: 48px;
            margin-bottom: 10px;
            display: inline-block;
        }
        h1 {
            font-size: 24px;
            color: #1a1a1a;
            margin-bottom: 8px;
            font-weight: 600;
        }
        .subtitle {
            font-size: 14px;
            color: #666;
            margin-bottom: 25px;
        }
        /* 价格表格 */
        .table-container {
            overflow-x: auto;
            margin-bottom: 25px;
            border-radius: 8px;
            border: 1px solid #eaeaea;
        }
        table {
            width: 100%;
            border-collapse: collapse;
            font-size: 14px;
        }
        th, td {
            padding: 12px 8px;
            text-align: center;
            border-bottom: 1px solid #eaeaea;
        }
        th {
            background-color: #f8fafc;
            color: #475569;
            font-weight: 500;
        }
        td {
            color: #334155;
        }
        tr:last-child td { border-bottom: none; }
        .price {
            color: #e11d48; /* 价格红色高亮 */
            font-weight: 600;
        }
        /* 按钮通用样式 */
        .btn {
            display: block;
            width: 100%;
            padding: 14px 0;
            border-radius: 8px;
            font-size: 16px;
            font-weight: 500;
            text-decoration: none;
            cursor: pointer;
            transition: all 0.2s ease;
            border: none;
            margin-bottom: 12px;
        }
        /* 主按钮（跳转注册） */
        .btn-primary {
            background-color: #2563eb; /* 科技蓝 */
            color: #ffffff;
            box-shadow: 0 4px 12px rgba(37, 99, 235, 0.3);
        }
        .btn-primary:active {
            transform: scale(0.98);
        }
        /* 副按钮（复制微信） */
        .btn-secondary {
            background-color: #f1f5f9;
            color: #475569;
            border: 1px solid #e2e8f0;
        }
        .btn-secondary:active {
            background-color: #e2e8f0;
        }
        /* 复制成功的提示状态 */
        .btn-secondary.copied {
            background-color: #10b981;
            color: white;
            border-color: #10b981;
        }
        /* 页脚提示 */
        .footer-tips {
            margin-top: 20px;
            font-size: 12px;
            color: #94a3b8;
        }
    </style>
</head>
<body>

    <div class="card">
        <!-- 图标与标题 -->
        <div class="icon">🌐</div>
        <h1>优众代理平台</h1>
        <p class="subtitle">国内静态IP · 游戏低延迟专线 · 免费测试</p >

        <!-- 价格表格 -->
        <div class="table-container">
            <table>
                <thead>
                    <tr>
                        <th>套餐类型</th>
                        <th>带宽</th>
                        <th>参考价</th>
                    </tr>
                </thead>
                <tbody>
                    <tr>
                        <td>SK5 电信A区</td>
                        <td>5-10M</td>
                        <td class="price">6.00 元/月</td>
                    </tr>
                    <tr>
                        <td>SK5 腾讯云</td>
                        <td>5-10M</td>
                        <td class="price">6.00 元/月</td>
                    </tr>
                    <tr>
                        <td>L2TP 电信A区</td>
                        <td>5-10M</td>
                        <td class="price">11.00 元/月</td>
                    </tr>
                    <tr>
                        <td>L2TP 电信B区</td>
                        <td>10-20M</td>
                        <td class="price">15.00 元/月</td>
                    </tr>
                </tbody>
            </table>
        </div>

        <!-- 动作按钮 -->
        <!-- 这是你的专属注册链接，已经填好了 -->
        <a href=" " target="_blank" class="btn btn-primary">
            🚀 点击前往注册 / 免费测试
        </a >

        <!-- 复制微信按钮 -->
        <button onclick="copyWeChat()" id="copyBtn" class="btn btn-secondary">
            📋 复制客服微信号：lzx24ad
        </button>

        <div class="footer-tips">
            * 注册后如需指导配置，请添加客服微信
        </div>
    </div>

    <!-- 复制功能的 JavaScript 代码 -->
    <script>
        function copyWeChat() {
            // 这里填入你要复制的微信号
            const wechatId = "lzx24ad"; 
            const btn = document.getElementById("copyBtn");

            if (navigator.clipboard) {
                navigator.clipboard.writeText(wechatId).then(() => {
                    showSuccess(btn);
                }).catch(() => {
                    fallbackCopy(wechatId, btn);
                });
            } else {
                fallbackCopy(wechatId, btn);
            }
        }

        function fallbackCopy(text, btn) {
            const textArea = document.createElement("textarea");
            textArea.value = text;
            textArea.style.position = "fixed";
            document.body.appendChild(textArea);
            textArea.select();
            try {
                document.execCommand('copy');
                showSuccess(btn);
            } catch (err) {
                alert('复制失败，请手动复制：' + text);
            }
            document.body.removeChild(textArea);
        }

        function showSuccess(btn) {
            const originalText = btn.innerHTML;
            btn.classList.add("copied");
            btn.innerHTML = "✅ 微信号已复制，去微信添加吧";
            setTimeout(() => {
                btn.classList.remove("copied");
                btn.innerHTML = originalText;
            }, 2500);
        }
    </script>

</body>
</html>
