# Create Contracted Company with Timizer

Creates a contracted company in Timizer.

## Endpoint

- **Method:** `POST`
- **Path:** `/app/contracted`
- **Base URL:** `https://api.timizer.io`
- **Official documentation:** [Create Contracted Company](https://api-doc.timizer.io)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `city` | body | `string` | no | City of the contracted company. |
| `fullAddress` | body | `string` | no | Full address of the contracted company. |
| `name` | body | `string` | yes | Name of the contracted company. |
| `postalCode` | body | `string` | no | Postal code of the contracted company. |
| `teamId` | body | `number` | no | Team ID to make the contracted company available to the team. |
| `uniqueIdentifier` | body | `string` | no | Unique identifier of the contracted company. |
