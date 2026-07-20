# Create Client with Timizer

Creates a client in Timizer.

## Endpoint

- **Method:** `POST`
- **Path:** `/app/clients`
- **Base URL:** `https://api.timizer.io`
- **Official documentation:** [Create Client](https://api-doc.timizer.io)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `city` | body | `string` | no | City of the client. |
| `country` | body | `string` | no | Country code alpha-2 of the client. |
| `fullAddress` | body | `string` | no | Full address of the client. |
| `name` | body | `string` | yes | Name of the client. |
| `postalCode` | body | `string` | no | Postal code of the client. |
| `teamId` | body | `number` | no | Team ID to make the client available to the team. |
| `uniqueIdentifier` | body | `string` | no | Unique identifier of the client. |
