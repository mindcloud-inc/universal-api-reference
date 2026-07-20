# List Subscriptions with MoneyBird

Retrieves subscriptions from MoneyBird.

## Endpoint

- **Method:** `GET`
- **Path:** `/:administrationId/subscriptions.json`
- **Base URL:** `https://moneybird.com/api/v2`
- **Official documentation:** [List Subscriptions](https://developer.moneybird.com/integration/managing-subscriptions)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `administrationId` | path | `string` | yes | Moneybird administration ID. |
| `contact_id` | query | `string` | yes | Moneybird contact ID used to list subscriptions for one contact. |
