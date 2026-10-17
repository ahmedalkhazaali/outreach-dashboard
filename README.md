# Freelance Outreach Dashboard

A live look at my cold-email outreach campaign to local small businesses — built and run in public.

I'm a Carleton University software engineering student reaching out to small business owners with a simple offer: tell me the problems costing you money, and I'll build a free solution to prove it saves you money before we talk pricing.

## Live dashboard

**[View the dashboard](https://ahmedalkhazaali.github.io/freelance-outreach-dashboard/)** — updated as leads are collected, validated, and emailed.

Or run it locally:

```bash
git clone https://github.com/ahmedalkhazaali/freelance-outreach-dashboard.git
cd freelance-outreach-dashboard
python3 -m http.server 8000
# open http://localhost:8000
```

No build step, no dependencies — it's a single static page reading `data.json`.

## How the campaign works

| Stage | What's happening |
|---|---|
| Collecting | Agents gather publicly listed contact emails from Ottawa & GTA small businesses (trades, clinics, restaurants, salons, professional services…) |
| Validating | A separate agent dedupes by business and verifies every email (format + MX record checks) before anything is sent |
| Sending | Validated leads get a personal outreach email — staggered in small batches, never blasted |
| Replies | Responses tracked here as they come in |

Only publicly published business contact emails are used. One email per business, no spam.

## Repo layout

```
index.html   — the dashboard (static, zero dependencies)
data.json    — live campaign data; refreshed as the pipeline moves
```

## Status

See the dashboard for live numbers. `data.json` carries an `updated_at` timestamp so you always know how fresh it is.

---
*Built with the help of Muse. Campaign run by Ahmed Al-Khazaali.*
