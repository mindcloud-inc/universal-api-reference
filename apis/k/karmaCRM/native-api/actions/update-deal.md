# Update Deal with Karma CRM

Updates an existing deal in Karma CRM.

## Endpoint

- **Method:** `PUT`
- **Path:** `/api/v3/deals/:id.json`
- **Base URL:** `https://app.karmacrm.com`
- **Official documentation:** [Update Deal](https://docs.karmacrm.com/#update-a-deal)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | The ID of the deal to update. |
| `deal` | body | `object` | yes | Deal payload object with the fields to update. |
