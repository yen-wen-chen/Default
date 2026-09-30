# DigWise GPU 環境登入教學

適用對象:參與 DigWise–NTU Self-Evolving Agentic-EDA 合作專案的學生。

依序完成 **Part 1 (SSLVPN)** → **Part 2 (GPU Server 遠端桌面)**,兩者缺一不可,因為 GPU Server 是內網位址,沒有先連上 VPN 無法連線。

## 帳號密碼

實際帳號密碼請洽專案窗口取得,**不要**把明文密碼提交進版本控制。下方以佔位符表示:

| 用途 | 帳號 | 密碼 |
|---|---|---|
| SSLVPN 登入 | `<student_account>` | `<sslvpn_password>` |
| GPU Server 遠端桌面登入 | `<student_account>` | `<gpu_server_password>` |

> 注意:SSLVPN 密碼與 GPU Server 密碼**不是同一組**,結尾的特殊符號可能不同,請分別確認。

## Part 1:SSLVPN 登入

1. 瀏覽器開啟:`https://sslvpn.digwise-tech.com:4443`
   - 出現憑證警告(內部自簽憑證)屬正常現象,選擇「進階」→「繼續前往」。
2. 若提示安裝 SSL-VPN 用戶端(如 FortiClient),依提示完成安裝。
3. 輸入帳號與密碼,點擊登入,建立 VPN 通道。
4. 確認工具列出現 VPN 已連線圖示。

### 常見登入失敗排查

- 密碼是否誤用全形符號?請切換至英數半形輸入法。
- 多次嘗試失敗可能觸發帳號鎖定,稍待後再試,或聯絡窗口協助解鎖。
- Port `4443` 若被所在網路的防火牆阻擋,可更換網路環境(如改用行動熱點)測試。

## Part 2:連線 GPU Server(遠端桌面)

前提:VPN 需保持連線中。

1. 開啟遠端桌面工具:
   - Windows:「遠端桌面連線」(mstsc)
   - Mac:「Microsoft Remote Desktop」(App Store 下載)
2. 電腦/IP 位址輸入:`10.25.0.66`(主機名稱:DW-Server-GPU)
3. 輸入帳號密碼並連線;若出現憑證警告,選擇「是 / 繼續連線」。

## 仍無法登入時,回報下列資訊

- 卡在 Part 1 或 Part 2
- 完整錯誤訊息或截圖
- 作業系統與網路環境

可聯繫專案窗口(見合作簡報第 2 頁 Q&A 聯絡窗口)協助排查。
