# 🔥 Free Fire Automated Spinning Tool

This is an automated Python tool designed to spin Gacha events on Free Fire using Guest Accounts. It supports multiple servers, automatic retry logic, and saves rare item hits.

## 📂 Required Files
Ensure all these files are in the same folder before running:
1. `GojoBundleSpinV2.py` (The main script)
2. `my_pb2.py` (Required for login encryption)
3. `output_pb2.py` (Required for decoding responses)
4. `guestAcc.json` (Your list of accounts)

---

## 🛠️ Troubleshooting & Errors

If you encounter errors while running the script, please read the solutions below:

### 1. HTTP 400 Error ❌
If the logs show **[✗] Error: HTTP 400**, it usually means one of the following:
*   **Account is not activated:** The Guest Account is fresh and hasn't been initialized. **Solution:** Run `activator.py` first to activate the accounts.
*   **Account is too old:** The Guest Account has expired or invalid credentials.
*   **Already Spun:** The spin/event reward has already been claimed on this specific account.

### 2. [✗] Error: Connection Fail 🌐
This error indicates a problem with your **Internet Connection**.
*   Check your Wi-Fi or Data connection.
*   The script cannot reach the game servers.

### 3. Server Timeout / Region Issues 🌍
If the script fails to connect to a specific region (e.g., US, NA, SAC) or keeps timing out:
*   **Check Manual Access:** Try opening the Free Fire game on your mobile using that region's guest account.
*   **VPN Required:** If the game **does not open** on your mobile for that region without a VPN, the script won't work either.
*   **Solution:** Connect your device to a **VPN** matching the target server (e.g., if spinning on the **US Server**, connect your VPN to **USA**) and try again.

---

## 🚀 How to Use

1. **Install Requirements:**
   The script will auto-install missing libraries, but you can manually install them:
   ```bash
   pip install aiohttp blackboxprotobuf pycryptodome requests

1: Prepare Accounts (guestAcc.json):
Make sure your guestAcc.json follows this format:

[
  {
    "uid": "4416710682",
    "password": "SK_51413_BY_SPIDEERIO_GAMING_ZJF23",
    "account_id": "14479881056",
    "name": "SK⁹⁸²³⁴",
    "region": "BD",
    "status": "activated"
  },
  {
    "uid": "4416710566",
    "password": "SK_JSBGR_BY_SPIDEERIO_GAMING_UTQJX",
    "account_id": "14479880583",
    "name": "SK¹⁸⁸⁰²",
    "region": "BD",
    "status": "activated"
  },
  {
    "uid": "4416711945",
    "password": "SK_CG0MU_BY_SPIDEERIO_GAMING_MH8SG",
    "account_id": "14479886346",
    "name": "SK⁶⁶⁰⁸³",
    "region": "BD",
    "status": "activated"
  }
]

Run the Script:

python GojoBundleSpinV2.py

Select Region:
Choose the correct server number (e.g., 1 for India, 2 for Brazil, etc.).

Stop the Script:
Press CTRL + C to stop. The script will automatically save your logs and results before closing.

📝 Output Files

special_id.json: Saves rare items found (Live update).

summary_list.txt: A clean list of UIDs and Passwords that got items.

decoded_output.txt: Raw server response data (Saved at the end).

terminal_log.txt: Full log of the session (Saved at the end).

⚠️ Disclaimer

This tool is for educational purposes only. Use it responsibly.

In Last I want to tell What Is This👇
[?] Start from Account Number (Default 1):
If You Have 2000 Accounts and 1200 Accounts Already Spinned If You choose
[?] Start from Account Number (Default 1): 1201
Than Script Will Start Spinning From Account 1201 Not From 1.

If any Error Personal Dm Telegram @ShamNpl