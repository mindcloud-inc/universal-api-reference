# Create Search with Melo

Creates a new search in Melo.

## Endpoint

- **Method:** `POST`
- **Path:** `/searches`
- **Base URL:** `https://preprod-api.notif.immo`
- **Official documentation:** [Create Search](https://docs.melo.io/api-reference/endpoint/searches/create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `title` | body | `string` | yes | Search title. |
| `transactionType` | body | `number` | yes | Transaction type: 0 sell, 1 rent. |
| `propertyTypes[]` | body | `array<number>` | yes | Property type IDs. |
| `includedDepartments[]` | body | `array<string>` | yes | Department resource IDs to include, for example /departments/77. |
| `budgetMax` | body | `number` | yes | Maximum budget amount. |
