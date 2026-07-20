# Get Bulk Number Lookup Status with SMS Connexion

Retrieves a bulk number lookup result from SMS Connexion.

## Endpoint

- **Method:** `GET`
- **Path:** `/numbers/lookup/lookupBulkId/:lookupBulkId`
- **Base URL:** `https://api.sms.cx`
- **Official documentation:** [Get Bulk Number Lookup Status](https://sms.cx/sms-api-documentation/#operation/GetBulkLookupStatus)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `lookupBulkId` | path | `string` | yes | Bulk lookup UUID. |
