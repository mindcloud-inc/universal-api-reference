# Update Contracted Company with Timizer

Updates an existing contracted company in Timizer.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/app/contracted/:id`
- **Base URL:** `https://api.timizer.io`
- **Official documentation:** [Update Contracted Company](https://api-doc.timizer.io)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `archived` | body | `boolean` | no | Whether the contracted company is archived. |
| `city` | body | `string` | no | Updated city of the contracted company. |
| `fullAddress` | body | `string` | no | Updated full address of the contracted company. |
| `id` | path | `number` | yes | ID of the contracted company. |
| `name` | body | `string` | no | Updated name of the contracted company. |
| `postalCode` | body | `string` | no | Updated postal code of the contracted company. |
| `uniqueIdentifier` | body | `string` | no | Updated unique identifier of the contracted company. |
