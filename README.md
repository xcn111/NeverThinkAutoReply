# Never Think Auto Reply

[![Releases Badge](https://img.shields.io/github/downloads/RyuuMeow/NeverThinkAutoReply/total)](https://github.com/RyuuMeow/NeverThinkAutoReply/releases)
[![Latest Release](https://img.shields.io/github/v/release/RyuuMeow/NeverThinkAutoReply)](https://github.com/RyuuMeow/NeverThinkAutoReply/releases/latest)

### 一個方便的快速回覆工具，搭配快捷鍵叫出，形成一個懶人回覆鏈
### 多種智慧回覆模式，包括自動MyGo、Mujica、正常、反駁、嘲諷，全程無需使用者動腦

![](assets/demo/img1.png)

> [!NOTE]
> 於2.2版新增 "Ave Mujica功能"

## 效果演示

https://youtu.be/67BNZq99TI8
https://youtu.be/bpvHgRAo-eE

[<video src='https://youtu.be/67BNZq99TI8' width=180/>](https://github.com/user-attachments/assets/8d59fc0b-874d-4769-bb89-fcaa0746941b)

[<video src='https://youtu.be/bpvHgRAo-eE' width=180/>](https://github.com/user-attachments/assets/d1a4e4d6-97b6-4c94-88d1-bd722eef82a0)

![](assets/demo/img2.png)
![](assets/demo/img3.png)

---

## 功能特點

- 全局快捷鍵叫出 (預設 Ctrl+Shift+X)
- 支援多種回覆模式：
  - 正常回覆
  - 反駁模式
  - 嘲諷模式
  - MyGO 表情貼圖
- 自動複製貼上功能
- 自動隱藏功能

## 主要依賴

- PySide6
- pyperclip
- pyautogui
- pynput
- windows-toasts
- pywin32
- openai

---

## 前置準備

1. 右鍵使用記事本打開`config.ini`
2. (可選)選擇主要模型 (openai, gemini, deepseek) (預設為openai)
```bash
[General]
base_model = openai
```
> [!NOTE]
> 於2.1版新增 "模型切換功能"

3. 貼上 API Key (假設主要模型使用openai)
```bash
[Keys]
openai = 你的OpenAI API Key
```

---

## (推薦)使用方法 1 - 使用已打包版本(從右側Releases下載)

1. 運行程式：(建議)使用系統管理員 打開app.exe
2. 基本操作流程：
   - 反白要回覆的文字
   - 按下快捷鍵 `Ctrl+Shift+X` 叫出選單
   - 選擇回覆模式
   - 等待Windows通知提示出現(需等待0.5至1秒不等)
   - 點選要貼上的位置(輸入框)
   - 程式會自動處理並貼上回覆內容

### 開機自啟動設定
1. 右鍵使用記事本開啟`NTAR_Run.bat`
2. 將路徑替換為app.exe的絕對路徑 並儲存
3. 將`NTAR_Run.bat`移動至`C:\Users\你的使用者名稱\AppData\Roaming\Microsoft\Windows\Start Menu\Programs\Startup`
   (可直接於檔案總管路經欄搜尋startup)

## 使用方法 2 - Clone Repo

1. 安裝依賴

```bash
pip install -r requirements.txt
```

2. 運行程式：

```bash
python NeverThinkAutoReply.py
```

3. 基本操作流程： 同上

---

## 自己加圖片

將圖片丟至 `assets/mygo` 或 `assets/mujica` 底下

> [!NOTE]
> 於2.2版新增 "添加圖片功能"

---

## 自訂配置

您可以在config.ini中修改以下設定：

- 快捷鍵：修改General類之 `hotkey` 參數
- 模型切換：修改General類之 `base_model` 參數
- API金鑰：修改Keys類之 `openai`、`gemini`、`deepseek` 參數

---

## 系統需求

- 作業系統：Windows 10+

  或

- Python 3.9+

---

## 注意事項

- 程式可能需要管理員權限來監聽全局快捷鍵
- 請確保系統剪貼簿功能正常

---

## 問題回報

如果您在使用過程中遇到任何問題，請在 Issues 中回報。

---

## 圖片來源

- https://forum.gamer.com.tw/Co.php?bsn=60076&sn=96559036
- https://github.com/serser322/ave-mujica-images
