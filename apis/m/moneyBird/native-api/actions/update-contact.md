# Update Contact with MoneyBird

Updates an existing contact in MoneyBird.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/:administrationId/contacts/:contactId.json`
- **Base URL:** `https://moneybird.com/api/v2`
- **Official documentation:** [Update Contact](https://developer.moneybird.com/api/contacts)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `administrationId` | path | `string` | yes | Moneybird administration ID. |
| `contactId` | path | `string` | yes | Moneybird contact ID. |
