# Get Number Lookup Status with SMS Connexion

Retrieves a number lookup result from SMS Connexion.

## Endpoint

- **Method:** `GET`
- **Path:** `/numbers/lookup/lookupId/:lookupId`
- **Base URL:** `https://api.sms.cx`
- **Official documentation:** [Get Number Lookup Status](https://sms.cx/sms-api-documentation/#operation/GetSingleLookupStatus)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `lookupId` | path | `string` | yes | Lookup UUID. |
