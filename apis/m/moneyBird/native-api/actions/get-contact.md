# Get Contact with MoneyBird

Retrieves a contact from MoneyBird.

## Endpoint

- **Method:** `GET`
- **Path:** `/:administrationId/contacts/:contactId.json`
- **Base URL:** `https://moneybird.com/api/v2`
- **Official documentation:** [Get Contact](https://developer.moneybird.com/api/contacts)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `administrationId` | path | `string` | yes | Moneybird administration ID. |
| `contactId` | path | `string` | yes | Moneybird contact ID. |
