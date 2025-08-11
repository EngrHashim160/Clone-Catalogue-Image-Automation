# 🌸 Clone Catalogue Image Automation

This n8n workflow automates the enhancement of product images from a Google Sheets catalogue. It downloads original images, processes them using **Replicate’s Flux-Kontext-Pro AI model** for premium e-commerce quality, uploads them to Google Drive, and updates the Google Sheet with the new public image links.

---

## 🚀 Features

- 📥 **Fetch Data** from Google Sheets with row tracking.
- 🖼 **Download Original Images** from provided URLs.
- 🤖 **AI Image Enhancement** using Replicate’s Flux-Kontext-Pro model.
- ⏳ **Wait & Status Check** for asynchronous AI processing.
- ☁ **Upload to Google Drive** and auto-share publicly.
- ✏ **Update Google Sheets** with processed image links.
- 🔄 Handles multiple catalogue items in a batch.

---

## 📂 Workflow Overview

1. **Webhook Trigger** — Starts automation when triggered.
2. **Read Google Sheets** — Retrieves catalogue rows.
3. **Filter** — Skips rows with empty image URLs.
4. **Download Original Image** — Gets image from URL.
5. **AI Processing** — Sends to Replicate API with a prompt for professional floral photography.
6. **Status Polling** — Waits for AI to finish processing.
7. **Download Processed Image** — Retrieves enhanced result.
8. **Upload to Google Drive** — Saves processed image.
9. **Make Public** — Generates shareable link.
10. **Update Google Sheets** — Writes back the new image link.

---

## 🛠 Installation & Setup

1. **Import Workflow into n8n**:
   - Download the `.json` file or copy directly into n8n.
   
2. **Set Up Credentials in n8n**:
   - Google Sheets OAuth2 API
   - Google Drive OAuth2 API
   - Replicate API Token

3. **Edit Workflow Variables**:
   - Google Sheets document ID and sheet name
   - Google Drive destination folder ID
   - Replicate prompt (optional customization)

---

## 🔑 Environment Variables

| Variable            | Description                                   | Example Value                                       |
|---------------------|-----------------------------------------------|-----------------------------------------------------|
| `GOOGLE_SHEETS_ID`  | ID of your Google Sheet catalogue             | `1xbJmgYfm9_SX3ZawoUPVkBEulKHQkING1XEnkXrnBJk`       |
| `SHEET_NAME`        | Name or ID of the worksheet                   | `Floristería`                                       |
| `GOOGLE_DRIVE_ID`   | Destination Google Drive folder ID            | `1NR1LK6kuZ8Cv6tNNgFB8z42FN1AZfIuj`                  |
| `REPLICATE_API_KEY` | API key for Replicate                         | `r8_RbTFaaIM4hQybOohrohGQHP5MKBaLl3lMCSs`           |

---

## ▶ Usage

1. Trigger the webhook endpoint provided by n8n.
2. The workflow will:
   - Fetch product data from Google Sheets
   - Enhance each image with AI
   - Upload the result to Google Drive
   - Update the sheet with new public links

---

## 📌 Notes

- Ensure Google Drive has enough storage.
- Replicate API credits may apply for processing images.
- The AI prompt is tailored for floral product photography but can be customized for other catalogue types.

---

## 📜 License

This workflow is released under the MIT License.
