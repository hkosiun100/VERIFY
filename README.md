# MCD Online Verification Portal (www.mcdgov.online)

## How to Deploy on Separate GitHub & Separate Vercel Account
1. Upload the files in this ZIP (`index.html`, `vercel.json`, and `images/`) to the root of your separate GitHub repository.
2. Import that GitHub repository into your separate Vercel account and click **Deploy**.
3. In Vercel Project Settings -> **Domains**, add **`www.mcdgov.online`** (and `mcdgov.online`).
4. Optional: Place `logo.svg`, `s.png`, and `crs.png` inside the `/images/` folder of this repository so PDF downloads load logos directly from `www.mcdgov.online` (it also has an automatic fallback to your main portal).

## URL Structure
- Scanning any DOB Delhi QR code opens:
  `https://www.mcdgov.online/verify/<DOCUMENT_ID>`
- It automatically fetches the record from the `upeprint` Firebase database, displays the `Citizen - Portal` table & `View` modal, and downloads the exact `BIRTH.HTML` PDF when `Download` is clicked.
