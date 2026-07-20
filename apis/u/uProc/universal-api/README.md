# <img src="https://images.mindcloud.co/apps/icons/417-4177058-discover-any-social-profile-with-uproc-for-linkedin_1775043624617.png" alt="UProc logo" width="28" height="28"> UProc: Universal API

Run uProc data processors to validate, enrich, transform, and retrieve data across personal, company, communication, finance, product, text, internet, image, and utility categories.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/uProc/latest
- **Category:** Business Intelligence / Data Extraction
- **Actions:** 31
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://uproc.io
- **Vendor API docs:** https://docs.uproc.io/api/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Check Credit Card Checksum](actions/check-credit-card-checksum.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/uProc/latest/actions/check-credit-card-checksum?connectionId=$CONNECTION_ID&credit_card=4024007151839544" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (31)

### Address Match

| Action | Method | Description |
| --- | --- | --- |
| [Get Exact Address by Search](actions/get-exact-address-by-search.md) | GET |  |

### Address Validation

| Action | Method | Description |
| --- | --- | --- |
| [Check Exact Address Exists](actions/check-exact-address-exists.md) | GET |  |

### Adult Validation

| Action | Method | Description |
| --- | --- | --- |
| [Check Age Is Adult](actions/check-age-is-adult.md) | GET |  |

### Age Equality Validation

| Action | Method | Description |
| --- | --- | --- |
| [Check Ages Are Equal](actions/check-ages-are-equal.md) | GET |  |

### Age Greater Validation

| Action | Method | Description |
| --- | --- | --- |
| [Check Age Is Greater](actions/check-age-is-greater.md) | GET |  |

### Age Lower Or Equal Validation

| Action | Method | Description |
| --- | --- | --- |
| [Check Age Is Lower or Equal](actions/check-age-is-lower-or-equal.md) | GET |  |

### Age Lower Validation

| Action | Method | Description |
| --- | --- | --- |
| [Check Age Is Lower](actions/check-age-is-lower.md) | GET |  |

### Age Range Result

| Action | Method | Description |
| --- | --- | --- |
| [Get Age Range by Date](actions/get-age-range-by-date.md) | GET |  |

### Age Range Validation

| Action | Method | Description |
| --- | --- | --- |
| [Check Age Is Between](actions/check-age-is-between.md) | GET |  |

### Age Result

| Action | Method | Description |
| --- | --- | --- |
| [Get Age by Date](actions/get-age-by-date.md) | GET |  |

### Age Threshold Validation

| Action | Method | Description |
| --- | --- | --- |
| [Check Age Is Greater or Equal](actions/check-age-is-greater-or-equal.md) | GET |  |

### Asin Existence Validation

| Action | Method | Description |
| --- | --- | --- |
| [Check ASIN Exists](actions/check-asin-exists.md) | GET |  |

### Asin Result

| Action | Method | Description |
| --- | --- | --- |
| [Get ASIN by EAN](actions/get-asin-by-ean.md) | GET |  |

### Asin Validation

| Action | Method | Description |
| --- | --- | --- |
| [Check ASIN Is Valid](actions/check-asin-is-valid.md) | GET |  |

### Bank Account Validation

| Action | Method | Description |
| --- | --- | --- |
| [Check ES Bank Account Is Valid](actions/check-es-bank-account-is-valid.md) | GET |  |

### Bic Validation

| Action | Method | Description |
| --- | --- | --- |
| [Check BIC Is Valid](actions/check-bic-is-valid.md) | GET |  |

### Card Number Validation

| Action | Method | Description |
| --- | --- | --- |
| [Check Credit Card Checksum](actions/check-credit-card-checksum.md) | GET |  |

### Coordinate Validation

| Action | Method | Description |
| --- | --- | --- |
| [Check Coordinates Are Valid](actions/check-coordinates-are-valid.md) | GET |  |

### Coordinates Result

| Action | Method | Description |
| --- | --- | --- |
| [Get Coordinates by Search](actions/get-coordinates-by-search.md) | GET |  |

### Credit Card Type Result

| Action | Method | Description |
| --- | --- | --- |
| [Get Credit Card Type by Number](actions/get-credit-card-type-by-number.md) | GET |  |

### Forties Validation

| Action | Method | Description |
| --- | --- | --- |
| [Check Age Is in the Forties](actions/check-age-is-in-the-forties.md) | GET |  |

### Iban Lookup Result

| Action | Method | Description |
| --- | --- | --- |
| [Get IBAN Lookup](actions/get-iban-lookup.md) | GET |  |

### Iban Result

| Action | Method | Description |
| --- | --- | --- |
| [Get IBAN by Account](actions/get-iban-by-account.md) | GET |  |

### Iban Validation

| Action | Method | Description |
| --- | --- | --- |
| [Check IBAN Is Valid](actions/check-iban-is-valid.md) | GET |  |

### Normalized Address

| Action | Method | Description |
| --- | --- | --- |
| [Get Normalized Address](actions/get-normalized-address.md) | GET |  |

### Parsed Address

| Action | Method | Description |
| --- | --- | --- |
| [Get Parsed Address](actions/get-parsed-address.md) | GET |  |

### Retirement Validation

| Action | Method | Description |
| --- | --- | --- |
| [Check Age Is Retired](actions/check-age-is-retired.md) | GET |  |

### Speech Result

| Action | Method | Description |
| --- | --- | --- |
| [Get Advanced Speech by Text](actions/get-advanced-speech-by-text.md) | GET |  |
| [Get Speech by Text](actions/get-speech-by-text.md) | GET |  |

### Street Number Validation

| Action | Method | Description |
| --- | --- | --- |
| [Check Street Number Exists](actions/check-street-number-exists.md) | GET |  |

### Twenties Validation

| Action | Method | Description |
| --- | --- | --- |
| [Check Age Is in the Twenties](actions/check-age-is-in-the-twenties.md) | GET |  |

