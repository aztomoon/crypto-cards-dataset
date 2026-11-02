# Cardipays crypto card dataset

Fees, FX markup, cashback, top-up costs and regions for 47 crypto debit cards. Maintained by [Cardipays](https://cardipays.xyz/), a crypto card checker that compares what a card promises with what real receipts show.

Updated: 2026-11-02.

## Files

- `cards.csv`, `cards.json`: one row per card, terms as the issuer describes them (text)
- `rates.csv`, `rates.json`: 88 rows, one per card tier, numbers ready for calculations

## Fields: cards

| Field | Meaning |
|---|---|
| `id`, `name`, `website` | card identifier, name, issuer site |
| `network` | Visa or Mastercard, if stated |
| `regions` | where the card is offered |
| `cashback`, `issuance`, `annual_fee`, `topup_fee`, `atm_fee`, `fx` | terms from the issuer |
| `notes` | bonuses and who the card suits best |

## Fields: rates

| Field | Meaning |
|---|---|
| `card`, `tier` | card and plan |
| `cashback_percent` | base cashback, percent |
| `fx_percent` | markup on non-USD spending, percent |
| `topup_fee_percent` | top-up or spend fee, percent |
| `cost`, `cashback_cap`, `payout` | price of the tier, cashback limits, how cashback is paid |
| `regions`, `excluded_countries` | availability, ISO country codes |
| `verified_by_issuer` | `true` if checked on the issuer's own help center, `false` if from third-party sources |

Empty value means the issuer does not state it. Terms change often: check the issuer before you sign up. Not financial advice.

## License

[CC BY 4.0](https://creativecommons.org/licenses/by/4.0/). Free to use, share and adapt, including commercially, with attribution:

> Data: Cardipays (https://cardipays.xyz/)
