# Collected on Tezos — data schema

Live file the app must fetch:

`https://raw.githubusercontent.com/be4con-nft/collected-on-tezos/main/data/monthly.json`

Backup cache (optional):

`https://cdn.jsdelivr.net/gh/be4con-nft/collected-on-tezos@main/data/monthly.json`

## Root

| field | meaning |
|---|---|
| meta | methodology and freshness |
| months | one object per closed calendar month, oldest first |

## meta

| field | meaning |
|---|---|
| as_of_month | last closed month in the file |
| period_start / period_end | chart range |
| updated_at | when this file was written |
| net_new_minters | null until that series is computed |

## months[]

| field | meaning |
|---|---|
| month | YYYY-MM |
| pieces | editions transferred in paid sales |
| sales | paid sale transactions |
| xtz | tez spent |
| usd | xtz × TzKT mid-month XTZ/USD |
| collectors | unique buyer wallets that month |
| sellers | unique seller wallets that month |
| avg_pieces_per_collector | pieces / collectors |
| avg_usd_per_collector | usd / collectors |

Do not sum collectors or sellers across months.
Net new minters are not in this file yet.
