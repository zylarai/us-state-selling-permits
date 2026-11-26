# US state seller's permits and state business licenses (50 states and DC, 2026)

Do you need a permit to sell at a craft fair, on Etsy or from a market stall, and what does it cost? For each US state and the District of Columbia, this dataset gives the registration a seller needs to collect sales tax (seller's permit, sales tax license, certificate of authority and so on): who issues it, what it costs, whether a deposit or bond can be required, whether it renews, the rules for temporary and event sellers, and whether the state also issues a general business license. Every value was checked on the state's own official pages (revenue or taxation department, comptroller, official forms, statutes and administrative rules) on November 23, 2026. Each row lists the official sources it came from.

Published by [Zylar](https://zylarai.com/?utm_source=github&utm_medium=referral&utm_campaign=dataset_selling_permits&utm_content=readme) under the [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/) licence. You can use, share and adapt it, including commercially, as long as you credit Zylar and link to the source.

**Permanent copy and citation (DOI):** [10.5281/zenodo.24483920](https://doi.org/10.5281/zenodo.24483920). Also on [Kaggle](https://www.kaggle.com/datasets/zylarai/us-sellers-permits-and-business-licenses-2026).

Companion dataset: [US state LLC formation and yearly fees](https://github.com/zylarai/us-state-llc-fees) (DOI [10.5281/zenodo.24404984](https://doi.org/10.5281/zenodo.24404984)).

## At a glance

- **No statewide sales tax, so no seller's permit:** Alaska, Delaware, Montana, New Hampshire and Oregon. Local sales taxes still apply in many Alaska towns, and Delaware requires a state business license.
- **Free to register:** 25 states, including California, Texas, Florida, New York and Georgia.
- **A fee to register:** 14 states, from $12 (Arizona, per location) to $100 (Connecticut).
- **Not confirmed on an official page:** the fee in 7 states (Kentucky, Louisiana, Massachusetts, Maryland, Minnesota, North Dakota, New Jersey). Those cells are empty and listed in `to_confirm`, not guessed.
- **A deposit or bond may be required:** in at least 17 states. The amount is usually set when you apply.
- **A general state business license:** confirmed in Alaska, Alabama (county-issued privilege license), DC, Delaware, Nevada, Washington and West Virginia. Elsewhere licenses are mostly local (city or county), so check there too.
- **Local registration on top of the state:** home-rule cities in Colorado, Louisiana parishes and Alaska boroughs and cities run their own sales tax.

## Files

| File | What it holds |
|---|---|
| `us-state-selling-permits.csv` | One row per state, all columns below. Lists inside a cell are separated by spaces (URLs) or semicolons (notes). |
| `us-state-selling-permits.json` | The same records as JSON, keyed by state code, with `official_sources` and `to_confirm` as arrays. |
| `LICENSE` | CC BY 4.0 legal text. |

## Columns

| Column | Meaning |
|---|---|
| `state`, `code` | State name and two-letter postal code |
| `statewide_sales_tax` | `yes` or `no` |
| `permit_name` | Official name of the registration a seller needs to collect sales tax |
| `permit_note` | Who needs it, and what applies instead in states with no sales tax |
| `agency` | Issuing agency |
| `permit_fee_usd` | Fee to register, in US dollars; `0` if free; empty if not confirmed |
| `permit_fee_note` | Details: per location, paper vs online, the official wording |
| `deposit_or_bond` | `none`, `may_be_required` or `required` |
| `renewal_rule`, `renewal_fee_usd` | Whether and when it renews, and the renewal fee |
| `temporary_permit` | Temporary or special event permit, its name and length |
| `event_seller_rule` | What craft fair, flea market and farmers market sellers must do |
| `local_registration` | Whether cities, counties or parishes require their own sales tax registration |
| `state_business_license` | `yes` or `no` if an official page says so; empty if not confirmed |
| `state_license_name`, `state_license_fee_usd`, `state_license_renewal`, `state_license_threshold` | The state general business license, where one exists |
| `local_license_note` | What official state pages say about city or county business licenses |
| `registration_url`, `faq_url` | Official online registration and FAQ or guide pages |
| `spanish_info_url` | Official Spanish-language page, where one was found |
| `official_sources` | Every official URL used for the row |
| `to_confirm` | Fields not confirmed on an official page, with the reason. Nothing here is guessed |
| `checked_on` | Date checked |
| `guide_page` | The matching state page in Zylar's free guide to starting a business |

## Notes and limits

- Sales tax only. Income tax, payroll and industry licenses (food, alcohol, tobacco, contractors) are out of scope.
- Several official sites block automated reading; some were read in a normal browser and some fields could not be confirmed. Where official pages disagree (for example Michigan's renewal date, West Virginia's registration threshold), both are noted.
- Rules and fees change. Check the official source before you register.
- This is general information, not legal or tax advice.
- Found an error or a change? Open an issue. We recheck the data regularly.

## How to cite

Zylar (2026). *US state seller's permits and state business licenses (50 states and DC, 2026)* (Version v2026.11) [Data set]. Zenodo. https://doi.org/10.5281/zenodo.24483920

## About Zylar

Zylar checks a business or startup idea before you build it: what the market says, who else does it, whether you can deliver it and what could go wrong, with a scored verdict in a few minutes. It is in early alpha and free to try: [sign up here](https://zylarai.com/?utm_source=github&utm_medium=referral&utm_campaign=dataset_selling_permits&utm_content=readme_about). Advisory only. You decide.
