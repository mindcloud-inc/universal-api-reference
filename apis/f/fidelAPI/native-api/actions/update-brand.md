# Update Brand with Fidel API

Updates an existing brand in Fidel API.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/brands/:brandId`
- **Base URL:** `https://api.fidel.uk/v1`
- **Official documentation:** [Update Brand](https://reference.fidel.uk/reference/update-brand)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `brandId` | path | `string` | yes | — |
| `websiteURL` | body | `string` | no | URL for the Brand. |
