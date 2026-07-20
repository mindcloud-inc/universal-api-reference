# <img src="https://images.mindcloud.co/apps/icons/s-msup_1776883439272.png" alt="SMSup logo" width="28" height="28"> SMSup: Universal API

Send SMS, verify numbers, manage balances, and run 2FA flows

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/sMSup/latest
- **Category:** Communication / Team Messaging
- **Actions:** 16
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.smsup.es/
- **Vendor API docs:** https://app.smsup.es/api/3.0/docs/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Account Balance](actions/get-account-balance.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sMSup/latest/actions/get-account-balance?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (16)

### Account Balance

| Action | Method | Description |
| --- | --- | --- |
| [Get Account Balance](actions/get-account-balance.md) | GET |  |

### Country Pricing

| Action | Method | Description |
| --- | --- | --- |
| [Get Country Pricing](actions/get-country-pricing.md) | GET |  |

### Hlr Lookup

| Action | Method | Description |
| --- | --- | --- |
| [Request HLR Lookup](actions/request-hlr-lookup.md) | GET |  |

### Pin Request

| Action | Method | Description |
| --- | --- | --- |
| [Request PIN](actions/request-pin.md) | POST |  |

### Pin Verification

| Action | Method | Description |
| --- | --- | --- |
| [Verify PIN](actions/verify-pin.md) | GET |  |

### Prefix Pricing

| Action | Method | Description |
| --- | --- | --- |
| [Get Prefix Pricing](actions/get-prefix-pricing.md) | GET |  |

### Sms Landing

| Action | Method | Description |
| --- | --- | --- |
| [Send SMS Landing](actions/send-sms-landing.md) | POST |  |

### Sms Link

| Action | Method | Description |
| --- | --- | --- |
| [Send SMS Link](actions/send-sms-link.md) | POST |  |

### Sms Message

| Action | Method | Description |
| --- | --- | --- |
| [Send SMS](actions/send-sms.md) | POST |  |

### Sms Survey

| Action | Method | Description |
| --- | --- | --- |
| [Send SMS Survey](actions/send-sms-survey.md) | POST |  |

### Subaccount

| Action | Method | Description |
| --- | --- | --- |
| [Create Subaccount](actions/create-subaccount.md) | POST |  |
| [Delete Subaccount](actions/delete-subaccount.md) | DELETE |  |

### Subaccount Balance

| Action | Method | Description |
| --- | --- | --- |
| [Add Subaccount Balance](actions/add-subaccount-balance.md) | PUT |  |
| [Deduct Subaccount Balance](actions/deduct-subaccount-balance.md) | PUT |  |
| [Get Subaccount Balance](actions/get-subaccount-balance.md) | GET |  |

### Subaccount Info

| Action | Method | Description |
| --- | --- | --- |
| [Get Subaccount Info](actions/get-subaccount-info.md) | GET |  |

