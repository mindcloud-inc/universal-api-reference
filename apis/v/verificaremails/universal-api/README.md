# <img src="https://images.mindcloud.co/apps/icons/cropped-icono-verificaremails-32x32_1775761213045.png" alt="Verificaremails logo" width="28" height="28"> Verificaremails: Universal API

Validate emails, run batch checks, and inspect account credits

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/verificaremails/latest
- **Category:** Communication / Email Communications
- **Actions:** 31
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.verificaremails.com
- **Vendor API docs:** https://dashboard.verificaremails.com/documentation/index.html

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get All Credits](actions/get-all-credits.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/verificaremails/latest/actions/get-all-credits?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (31)

### Address Batch Status

| Action | Method | Description |
| --- | --- | --- |
| [Get Address Batch Status](actions/get-address-batch-status.md) | GET | Retrieves an address batch validation status from Verificaremails. |

### Address Batch Validation

| Action | Method | Description |
| --- | --- | --- |
| [Create Address Batch Validation](actions/create-address-batch-validation.md) | POST | Creates an address batch validation in Verificaremails. |

### Address Validation Result

| Action | Method | Description |
| --- | --- | --- |
| [Validate Single Address Input](actions/validate-single-address-input.md) | GET | Retrieves an address validation result from Verificaremails. |

### Complete Name Batch Status

| Action | Method | Description |
| --- | --- | --- |
| [Get Complete Name Batch Status](actions/get-complete-name-batch-status.md) | GET | Retrieves a complete name batch validation status from Verificaremails. |

### Complete Name Validation Result

| Action | Method | Description |
| --- | --- | --- |
| [Validate Single Complete Name Input](actions/validate-single-complete-name-input.md) | GET | Retrieves a complete name validation result from Verificaremails. |

### Credit Balance

| Action | Method | Description |
| --- | --- | --- |
| [Get Address Credits](actions/get-address-credits.md) | GET | Retrieves available address verification credits from Verificaremails. |
| [Get All Credits](actions/get-all-credits.md) | GET | Retrieves available credits for all Verificaremails services. |
| [Get Complete Name Credits](actions/get-complete-name-credits.md) | GET | Retrieves available complete name credits from Verificaremails. |
| [Get Email Credits](actions/get-email-credits.md) | GET | Retrieves available email verification credits from Verificaremails. |
| [Get Fuzzy Search Name Credits](actions/get-fuzzy-search-name-credits.md) | GET | Retrieves available fuzzy search name credits from Verificaremails. |
| [Get Name Credits](actions/get-name-credits.md) | GET | Retrieves available name verification credits from Verificaremails. |
| [Get Phone Credits](actions/get-phone-credits.md) | GET | Retrieves available phone verification credits from Verificaremails. |
| [Get Phone MNP Credits](actions/get-phone-mnp-credits.md) | GET | Retrieves available phone MNP credits from Verificaremails. |
| [Get Phone Syntactic Credits](actions/get-phone-syntactic-credits.md) | GET | Retrieves available phone syntactic credits from Verificaremails. |

### Email Batch Status

| Action | Method | Description |
| --- | --- | --- |
| [Get Email Batch Status](actions/get-email-batch-status.md) | GET | Retrieves an email batch validation status from Verificaremails. |

### Email Batch Validation

| Action | Method | Description |
| --- | --- | --- |
| [Create Email Batch Validation](actions/create-email-batch-validation.md) | POST | Creates an email batch validation in Verificaremails. |

### Email Validation Result

| Action | Method | Description |
| --- | --- | --- |
| [Validate Single Email Input](actions/validate-single-email-input.md) | GET | Retrieves an email validation result from Verificaremails. |

### Fuzzy Search Name Batch Status

| Action | Method | Description |
| --- | --- | --- |
| [Get Fuzzy Search Name Batch Status](actions/get-fuzzy-search-name-batch-status.md) | GET | Retrieves a fuzzy search name batch validation status from Verificaremails. |

### Fuzzy Search Validation Result

| Action | Method | Description |
| --- | --- | --- |
| [Validate Single Fuzzy Search Name Input](actions/validate-single-fuzzy-search-name-input.md) | GET | Retrieves a fuzzy search name validation result from Verificaremails. |

### Name Batch Status

| Action | Method | Description |
| --- | --- | --- |
| [Get Name Batch Status](actions/get-name-batch-status.md) | GET | Retrieves a name batch validation status from Verificaremails. |

### Name Batch Validation

| Action | Method | Description |
| --- | --- | --- |
| [Create Name Batch Validation](actions/create-name-batch-validation.md) | POST | Creates a name batch validation in Verificaremails. |

### Name Validation Result

| Action | Method | Description |
| --- | --- | --- |
| [Validate Single Name Input](actions/validate-single-name-input.md) | GET | Retrieves a name validation result from Verificaremails. |

### Phone Batch Status

| Action | Method | Description |
| --- | --- | --- |
| [Get Phone Batch Status](actions/get-phone-batch-status.md) | GET | Retrieves a phone batch validation status from Verificaremails. |

### Phone Batch Validation

| Action | Method | Description |
| --- | --- | --- |
| [Create Phone Batch Validation](actions/create-phone-batch-validation.md) | POST | Creates a phone batch validation in Verificaremails. |

### Phone Mnp Batch Status

| Action | Method | Description |
| --- | --- | --- |
| [Get Phone MNP Batch Status](actions/get-phone-mnp-batch-status.md) | GET | Retrieves a phone MNP batch validation status from Verificaremails. |

### Phone Mnp Batch Validation

| Action | Method | Description |
| --- | --- | --- |
| [Create Phone MNP Batch Validation](actions/create-phone-mnp-batch-validation.md) | POST | Creates a phone MNP batch validation in Verificaremails. |

### Phone Mnp Validation Result

| Action | Method | Description |
| --- | --- | --- |
| [Validate Single Phone MNP Input](actions/validate-single-phone-mnp-input.md) | GET | Retrieves a phone MNP validation result from Verificaremails. |

### Phone Syntactic Batch Status

| Action | Method | Description |
| --- | --- | --- |
| [Get Phone Syntactic Batch Status](actions/get-phone-syntactic-batch-status.md) | GET | Retrieves a phone syntactic batch validation status from Verificaremails. |

### Phone Syntactic Batch Validation

| Action | Method | Description |
| --- | --- | --- |
| [Create Phone Syntactic Batch Validation](actions/create-phone-syntactic-batch-validation.md) | POST | Creates a phone syntactic batch validation in Verificaremails. |

### Phone Syntactic Validation Result

| Action | Method | Description |
| --- | --- | --- |
| [Validate Single Phone Syntactic Input](actions/validate-single-phone-syntactic-input.md) | GET | Retrieves a phone syntactic validation result from Verificaremails. |

### Phone Validation Result

| Action | Method | Description |
| --- | --- | --- |
| [Validate Single Phone Input](actions/validate-single-phone-input.md) | GET | Retrieves a phone validation result from Verificaremails. |

