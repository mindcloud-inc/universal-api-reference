# List Person Regulated Documents with Fleetworthy

## Endpoint

- **Method:** `GET`
- **Path:** `/people-documents/regulated/{personId}`
- **Base URL:** `https://apis.fleetworthy.com/compliance-api/v1`
- **Official documentation:** [List Person Regulated Documents](https://developer.fleetworthy.com/api-details#api=prod-compliance-v1&operation=get-people-documents-regulated-personid)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `personId` | path | `string` | yes | The Fleetworthy person UUID. |
| `isActive` | query | `boolean` | no | Return only active documents when enabled. |
