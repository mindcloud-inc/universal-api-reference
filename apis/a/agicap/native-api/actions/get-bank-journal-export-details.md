# Get Bank Journal Export Details with Agicap

Retrieves details for a bank journal export from Agicap.

## Endpoint

- **Method:** `GET`
- **Path:** `/public/treasury-bank-journal/v1/entities/:entityId/exports/:exportId`
- **Base URL:** `https://api.agicap.com`
- **Official documentation:** [Get Bank Journal Export Details](https://api.agicap.com/treasury-bank-journal/detailed_documentation.pdf)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `entityId` | path | `string` | yes | Agicap entity identifier. |
| `exportId` | path | `string` | yes | Unique export identifier returned by the export list action. |
