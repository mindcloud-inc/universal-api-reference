# <img src="https://images.mindcloud.co/apps/icons/quantum-digital-icon_1782394247494.png" alt="Quantum Digital logo" width="28" height="28"> Quantum Digital: Universal API

Create direct mail and print orders

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/quantumDigital/latest
- **Category:** Marketing / Advertising
- **Actions:** 15
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://quantumdigital.com
- **Vendor API docs:** https://developer.quantumdigital.com/docs

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Orders](actions/list-orders.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/quantumDigital/latest/actions/list-orders?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (15)

### Customers

| Action | Method | Description |
| --- | --- | --- |
| [Check Dashboard Access](actions/check-dashboard-access.md) | GET |  |
| [Get Account Extra Data](actions/get-account-extra-data.md) | GET |  |
| [Sign Up](actions/sign-up.md) | POST |  |
| [Update API Account Mode](actions/update-api-account-mode.md) | PUT |  |

### Files

| Action | Method | Description |
| --- | --- | --- |
| [List User Designs](actions/list-user-designs.md) | GET |  |

### Invoices

| Action | Method | Description |
| --- | --- | --- |
| [List Invoices](actions/list-invoices.md) | GET |  |

### Lists

| Action | Method | Description |
| --- | --- | --- |
| [List User Lists](actions/list-user-lists.md) | GET |  |

### Locations

| Action | Method | Description |
| --- | --- | --- |
| [List Provinces](actions/list-provinces.md) | GET |  |

### Orders

| Action | Method | Description |
| --- | --- | --- |
| [List Orders](actions/list-orders.md) | GET |  |

### Payment Methods

| Action | Method | Description |
| --- | --- | --- |
| [Create Payment Method](actions/create-payment-method.md) | POST |  |
| [Delete Payment Method](actions/delete-payment-method.md) | DELETE |  |
| [List Payment Methods](actions/list-payment-methods.md) | GET |  |
| [Update Payment Method](actions/update-payment-method.md) | PUT |  |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [Update Login Email](actions/update-login-email.md) | PUT |  |
| [Update Password](actions/update-password.md) | PUT |  |

