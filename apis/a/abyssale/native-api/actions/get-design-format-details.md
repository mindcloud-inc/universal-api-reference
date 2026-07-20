# Get Design Format Details with Abyssale

Retrieves design format details from Abyssale.

## Endpoint

- **Method:** `GET`
- **Path:** `/designs/:designId/formats/:formatSpecifier`
- **Base URL:** `https://api.abyssale.com`
- **Official documentation:** [Get Design Format Details](https://developers.abyssale.com/rest-api/designs/design-format-details)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `designId` | path | `string` | yes | Unique identifier of the design |
| `formatSpecifier` | path | `string` | yes | Format name or UID |
