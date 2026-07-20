# Update Client with Timizer

Updates an existing client in Timizer.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/app/clients/:id`
- **Base URL:** `https://api.timizer.io`
- **Official documentation:** [Update Client](https://api-doc.timizer.io)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `archived` | body | `boolean` | no | Whether the client is archived. |
| `city` | body | `string` | no | Updated city of the client. |
| `country` | body | `string` | no | Updated country code alpha-2 of the client. |
| `fullAddress` | body | `string` | no | Updated full address of the client. |
| `id` | path | `number` | yes | ID of the client. |
| `name` | body | `string` | no | Updated name of the client. |
| `postalCode` | body | `string` | no | Updated postal code of the client. |
| `uniqueIdentifier` | body | `string` | no | Updated unique identifier of the client. |
