# List Bank Journal Exports with Agicap

Retrieves previous bank journal exports from Agicap.

## Endpoint

- **Method:** `GET`
- **Path:** `/public/treasury-bank-journal/v1/entities/:entityId/exports`
- **Base URL:** `https://api.agicap.com`
- **Official documentation:** [List Bank Journal Exports](https://api.agicap.com/treasury-bank-journal/detailed_documentation.pdf)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `entityId` | path | `string` | yes | Agicap entity identifier. |
| `size` | query | `number` | no | Number of exports to return. Agicap documents a maximum of 100. |
| `after` | query | `date` | no | Return exports after this ISO 8601 date cursor or filter value. |
| `before` | query | `date` | no | Return exports before this ISO 8601 date cursor or filter value. |
