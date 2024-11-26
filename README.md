# 🌟 图片 API 使用文档

## 特点
- 支持横屏/竖屏/自适应三种模式，采用高速节点
- 图片格式为 **AVIF**，已收录 **6115 张**
- 提供超高清图片，最大分辨率可达 **14K**
- 部分图片经过超分处理
- 图片地址可直接用于需要填写图片地址的地方

**更新时间：2024/11/26**

---

## 📝 API 端点

### 1. 获取随机横屏图片
- **说明**：返回分辨率为 4K-14K 的随机横屏图片
- **浏览器行为**：直接访问时将显示图片预览页面

#### URL
- 标准路径：`GET https://api.rls.icu/horizontal`
- 中文路径：`GET https://api.rls.icu/横屏`

---

### 2. 获取随机竖屏图片
- **说明**：返回分辨率为 2K-10K 的随机竖屏图片
- **浏览器行为**：直接访问时将显示图片预览页面

#### URL
- 标准路径：`GET https://api.rls.icu/vertical`
- 中文路径：`GET https://api.rls.icu/竖屏`

---

### 3. 获取自适应图片
- **说明**：根据设备自动返回横屏或竖屏图片
- **浏览器行为**：直接访问时将显示图片预览页面

#### URL
- 标准路径：`GET https://api.rls.icu/adaptive`
- 中文路径：`GET https://api.rls.icu/自适应`

---

## 💻 使用示例

### HTML 使用
<!-- 基础图片使用 -->
<img src="https://api.rls.icu/horizontal" alt="随机横屏图片">

### JavaScript 使用
// 获取并显示图片
fetch('https://api.rls.icu/adaptive')
  .then(response => response.blob())
  .then(blob => {
    const img = document.createElement('img');
    img.src = URL.createObjectURL(blob);
    document.body.appendChild(img);
  });

### CSS 背景使用
.background {
  background-image: url('https://api.rls.icu/horizontal');
  background-size: cover;
  background-position: center;
}

---

## ⚠️ 注意事项
1. 本 API **仅供个人学习研究使用**，禁止用于商业用途。
2. **请求频率限制**：同一 IP 每秒最多 2 次请求。

