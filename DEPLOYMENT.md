# 🚀 部署指南

本項目支持多種部署方式，您可以根據需要選擇最適合的方案。

## 📱 GitHub Pages 部署（推薦）

### 自動部署
1. Fork 這個倉庫到您的GitHub賬戶
2. 進入倉庫設置 (Settings)
3. 滾動到 "Pages" 部分
4. 在 "Source" 下選擇 "Deploy from a branch"
5. 選擇 "main" 分支和 "/ (root)" 文件夾
6. 點擊 "Save"
7. 幾分鐘後，您的網站將在 `https://yourusername.github.io/aws-english` 可用

### 自定義域名（可選）
如果您有自己的域名：
1. 在倉庫根目錄創建 `CNAME` 文件
2. 在文件中添加您的域名（如：`aws-guide.yourdomain.com`）
3. 在您的DNS提供商處添加CNAME記錄指向 `yourusername.github.io`

## 🌐 其他部署選項

### 1. Netlify 部署
1. 登錄 [Netlify](https://netlify.com)
2. 點擊 "New site from Git"
3. 連接您的GitHub倉庫
4. 部署設置：
   - Build command: 留空
   - Publish directory: `/`
5. 點擊 "Deploy site"

### 2. Vercel 部署
1. 登錄 [Vercel](https://vercel.com)
2. 點擊 "New Project"
3. 導入您的GitHub倉庫
4. 保持默認設置
5. 點擊 "Deploy"

### 3. 本地服務器
如果您想在本地運行：

```bash
# 使用Python (Python 3)
python -m http.server 8000

# 使用Python (Python 2)
python -m SimpleHTTPServer 8000

# 使用Node.js
npx serve .

# 使用PHP
php -S localhost:8000
```

然後在瀏覽器中訪問 `http://localhost:8000`

## 📁 文件結構

```
aws-english/
├── index.html          # 主頁面文件
├── README.md           # 項目說明
├── LICENSE             # 許可證
├── CONTRIBUTING.md     # 貢獻指南
├── DEPLOYMENT.md       # 部署指南
└── .gitignore         # Git忽略文件
```

## 🔧 自定義配置

### 修改內容
- 所有內容都在 `index.html` 文件中
- 使用任何文本編輯器即可修改
- 修改後直接提交到GitHub，GitHub Pages會自動更新

### 添加新功能
1. 在HTML中添加新的結構
2. 在CSS中添加相應的樣式
3. 在JavaScript中添加交互邏輯

### 性能優化
- 所有資源都內聯在HTML中，無需額外的HTTP請求
- 圖片使用emoji，無需加載外部圖片文件
- CSS和JavaScript已經壓縮優化

## 🌍 CDN 加速（可選）

如果您需要更快的全球訪問速度：

### Cloudflare
1. 註冊 [Cloudflare](https://cloudflare.com) 賬戶
2. 添加您的域名
3. 更新DNS設置
4. 啟用CDN和緩存優化

### AWS CloudFront
1. 創建CloudFront分發
2. 設置源為您的GitHub Pages URL
3. 配置緩存策略
4. 更新DNS記錄

## 📊 分析和監控

### Google Analytics（可選）
在 `index.html` 的 `<head>` 部分添加：

```html
<!-- Google Analytics -->
<script async src="https://www.googletagmanager.com/gtag/js?id=GA_TRACKING_ID"></script>
<script>
  window.dataLayer = window.dataLayer || [];
  function gtag(){dataLayer.push(arguments);}
  gtag('js', new Date());
  gtag('config', 'GA_TRACKING_ID');
</script>
```

## 🔒 安全考慮

- 本項目是純靜態網站，無服務器端代碼
- 所有數據都在客戶端處理，無隱私風險
- 建議啟用HTTPS（GitHub Pages默認支持）

## 🆘 故障排除

### 常見問題

**Q: GitHub Pages沒有更新**
A: 檢查倉庫設置中的Pages配置，確保選擇了正確的分支

**Q: 自定義域名不工作**
A: 檢查CNAME文件和DNS設置，可能需要等待DNS傳播

**Q: 頁面顯示不正常**
A: 檢查瀏覽器控制台的錯誤信息，確保所有文件都正確加載

### 獲取幫助
- 查看GitHub Issues
- 提交新的Issue描述問題
- 參考GitHub Pages官方文檔

---

🎉 **恭喜！您的AWS英語指南現在已經成功部署！**
