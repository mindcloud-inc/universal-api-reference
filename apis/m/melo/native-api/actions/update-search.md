# Update Search with Melo

Updates an existing search in Melo.

## Endpoint

- **Method:** `PUT`
- **Path:** `/searches/:id`
- **Base URL:** `https://preprod-api.notif.immo`
- **Official documentation:** [Update Search](https://docs.melo.io/api-reference/endpoint/searches/update)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Search resource identifier. |
| `title` | body | `string` | yes | Search title. |
| `transactionType` | body | `number` | yes | Transaction type: 0 sell, 1 rent. |
| `propertyTypes[]` | body | `array<number>` | yes | Property type IDs. |
| `includedDepartments[]` | body | `array<string>` | yes | Department resource IDs to include, for example /departments/77. |
| `budgetMax` | body | `number` | yes | Maximum budget amount. |
