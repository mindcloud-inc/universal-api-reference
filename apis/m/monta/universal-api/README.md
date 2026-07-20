# <img src="https://images.mindcloud.co/apps/icons/captura-de-tela-2026-04-15-as-16_1776279860584.png" alt="Monta logo" width="28" height="28"> Monta: Universal API

Automate EV charging, dashboards, and Monta charge point data

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/monta/latest
- **Actions:** 14
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.monta.com
- **Vendor API docs:** https://docs.public-api.monta.com/reference/home

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Current Application](actions/get-current-application.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/monta/latest/actions/get-current-application?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (14)

### Afir Charge Point

| Action | Method | Description |
| --- | --- | --- |
| [List AFIR Charge Points](actions/list-afir-charge-points.md) | GET | Retrieves AFIR-compliant charge points from Monta. |

### Application

| Action | Method | Description |
| --- | --- | --- |
| [Get Current Application](actions/get-current-application.md) | GET | Retrieves the current application from Monta. |

### Charge

| Action | Method | Description |
| --- | --- | --- |
| [Get Charge](actions/get-charge.md) | GET | Retrieves a charge from Monta. |
| [List Charges](actions/list-charges.md) | GET | Retrieves charges from Monta. |
| [Start Charge](actions/start-charge.md) | POST | Starts a new charge in Monta. |
| [Stop Charge](actions/stop-charge.md) | PUT | Stops an active charge in Monta. |

### Charge Kwh Consumption

| Action | Method | Description |
| --- | --- | --- |
| [Get Charge KWh Consumption](actions/get-charge-kwh-consumption.md) | GET | Retrieves charge consumption breakdowns from Monta. |

### Charge Point

| Action | Method | Description |
| --- | --- | --- |
| [Get Charge Point](actions/get-charge-point.md) | GET | Retrieves a charge point from Monta. |
| [List Charge Points](actions/list-charge-points.md) | GET | Retrieves charge points from Monta. |

### Detected Location

| Action | Method | Description |
| --- | --- | --- |
| [Detect Location](actions/detect-location.md) | GET | Detects a user's location by IP address in Monta. |

### Evse Status

| Action | Method | Description |
| --- | --- | --- |
| [Get EVSE Status](actions/get-evse-status.md) | GET | Retrieves dynamic EVSE status from Monta. |

### Wallet

| Action | Method | Description |
| --- | --- | --- |
| [Get Personal Wallet](actions/get-personal-wallet.md) | GET | Retrieves your personal team wallet from Monta. |

### Wallet Transaction

| Action | Method | Description |
| --- | --- | --- |
| [Get Wallet Transaction](actions/get-wallet-transaction.md) | GET | Retrieves a wallet transaction from Monta. |
| [List Wallet Transactions](actions/list-wallet-transactions.md) | GET | Retrieves wallet transactions from Monta. |

