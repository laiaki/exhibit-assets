# 專案用途
本專案用於儲存展品的靜態資料資源，供行動導覽應用程式透過 QR Code 讀取後下載 JSON 描述檔案，再從中解析出：
  - 展品的 3D 模型（.glb / .gltf）
  - 展品的文字介紹
# 專案結構
```
  exhibit-assets/
  ├── dragon.glb              # 3D 模型 (GLB 格式)
  └── model.json              # JSON 描述該模型的文字與資源連結
```
# 事前準備：製作QR Code
1. 製作JSON，可以描述展品資訊與對應模型檔案位置
2. 上傳 JSON 與模型到可公開存取的伺服器
   - 建立 GitHub Repo → 開啟 GitHub Pages 功能 → 獲得公開 URL
3. 使用QR Code 產生工具，將第2步的URL生成QR Code

# 使用流程
1. 手機應用程式掃描展品旁的 QR Code。
2. QR Code 對應的 URL 指向 model.json
3. 應用程式從 JSON 中取得：
   - 模型檔案位置（GLB 或 GLTF）
   - 展品名稱與介紹文字
   - 可選的預覽圖片連結
4. 將資源下載並在應用程式內部以 3D 模型與圖文呈現。
