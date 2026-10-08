# List Person Company Documents with Fleetworthy

## Endpoint

- **Method:** `GET`
- **Path:** `/people-documents/company/:personId`
- **Base URL:** `https://apis.fleetworthy.com/compliance-api/v1`
- **Official documentation:** [List Person Company Documents](https://developer.fleetworthy.com/api-details#api=prod-compliance-v1&operation=get-people-documents-company-personid)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `personId` | path | `string` | yes | The unique identifier of the person. |
| `isActive` | query | `boolean` | no | When true, returns only active documents. When false, returns all documents. |
