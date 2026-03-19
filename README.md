# iGaming Fraud & Bonus Abuse Analytics Dashboard

A fraud detection and bonus abuse dashboard built in Excel, designed to 
simulate how a real iGaming risk team would monitor and investigate 
suspicious player activity.

## What It Does

The dashboard takes raw transaction and bonus data and runs each record 
through a scoring model to flag fraud risk and bonus abuse. It covers 
500 transactions and 200 bonus records across a 15-month dataset and 
auto-updates as the underlying data changes.

## Fraud Scoring Model

Each transaction gets a score out of 100 based on five behavioural signals:

| Signal | Points |
|---|---|
| Login country does not match registered country | +30 |
| Win ratio above 3x the bet amount | +25 |
| KYC verification missing | +20 |
| Bet amount above R1,000 | +15 |
| Unrecognised or unknown device | +10 |

Anything scoring 60 or above gets flagged as high risk.

## Bonus Abuse Scoring Model

Each bonus record is scored across four signals:

| Signal | Points |
|---|---|
| Multi-account behaviour detected | +35 |
| Wagering below 50% of bonus received | +30 |
| KYC verification missing | +20 |
| Early withdrawal above 60% of bonus | +15 |

Records scoring 50 or above are flagged for review.

## Dashboard Structure

- **Dashboard** — summary KPIs and 7 charts, auto-updated from raw data
- **Transactions** — 500 player records with individual fraud scores
- **Bonuses** — 200 bonus records with individual abuse scores
- **Fraud Alerts** — live alert centre tracking current risk counts

## What It Tracks

- High-risk transactions (score 60+)
- Location mismatches between registered and login country
- Bonus abuse flags
- Players without KYC verification
- Monthly transaction trends and bet volume
- Fraud score distribution across the portfolio

## Tools

Built entirely in Excel using advanced formulas and dynamic references. 
No external libraries or plugins required.

## Author

Anele Ngubane | github.com/Anele101 | anelengubane101@gmail.com