# 🧾 Universal Reconciliation Match Predictor

A smart, Streamlit-powered web app that lets you upload **any two transaction files** (CSV, Excel, or TXT), detects columns automatically, evaluates potential matches using machine learning, and outputs results with confidence scores.

Created by **Paddy**, a lifelong banker turned tech wizard — for learning, love of ledgers, and a bit of binary banter. ❤️💾

---

## 🚀 Features

* Upload two transaction files (MT910, ledger, or anything structured)
* Auto-detect columns (amount, date, currency, narration)
* Full cross-pairing: supports one-to-many and many-to-one logic
* ML-based matching with Random Forest classifier
* Match confidence score (%), prediction flags, and dashboard summary
* Download results in CSV
* Runs 100% in your browser using [Streamlit Cloud](https://streamlit.io/cloud)

---

## 📦 File Structure

```
recon-app/
├── app.py                  # Main Streamlit script
├── requirements.txt        # Python dependencies for Streamlit Cloud
├── sample_mt910.csv        # Example input file 1
├── sample_ledger.csv       # Example input file 2
└── README.md               # This file
```

---

## 📥 How to Run on Streamlit Cloud

1. Fork or clone this repo
2. Go to [https://streamlit.io/cloud](https://streamlit.io/cloud)
3. Sign in with GitHub and deploy your repo
4. Upload your files and view results live

> 💡 No local Python installation needed!

---

## 📄 Input File Expectations

The app detects columns automatically. Supported synonyms:

| Feature     | Column Name Examples                   |
| ----------- | -------------------------------------- |
| Amount      | `amount`, `amt`, `value`               |
| Date        | `date`, `txn_date`, `transaction_date` |
| Currency    | `currency`, `ccy`                      |
| Description | `desc`, `description`, `narration`     |

CSV, Excel (`.xls`, `.xlsx`) or text (`.txt`) with `|` separators are all supported.

---

## 📊 Summary Dashboard

After prediction, you’ll see:

* ✅ High confidence matches (90–100%)
* ⚠️ Medium confidence (70–89%)
* ❌ Low confidence (<70%)

The app will also show:

* Total transactions evaluated
* Match distribution
* Likely matches in a data table

---

## 🧠 ML Engine (for the curious)

A Random Forest Classifier is trained on-the-fly using engineered features like:

* `amount_diff`
* `date_diff`
* `currency_match`
* `desc_match`

This is for learning/demo purposes — feel free to plug in your own model or scoring logic.

---

## 🧪 Example Use Cases

* MT910 vs Ledger Entries
* Suspense account cleanup
* Manual upload audits
* Payment instruction vs settlement records
* Nostro reconciliation for internal banking teams

---

## ❤️ A Note from Paddy

This project is part of my lifelong journey through finance and tech. Built purely for learning and sharing — feel free to fork, remix, and throw your own spice in.

> In the end, reconciliation is more than accounting. It’s making peace between systems, stories, and sometimes... ourselves.

---

## 📬 Feedback

Got an idea, a feature request, or just want to send some binary love?
Open an issue, start a discussion, or ping me on [LinkedIn](https://www.linkedin.com).

01001100 01001111 01010110 01000101
