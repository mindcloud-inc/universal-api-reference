# List Properties with Rachio Smart Hose Timer

Retrieves property records from your Rachio account.

## Endpoint

- **Method:** `GET`
- **Path:** `https://cloud-rest.rach.io/property/listProperties/:userId`
- **Base URL:** `https://api.rach.io/1`
- **Official documentation:** [List Properties](https://rachio.readme.io/reference/propertyservice_listproperties)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `userId` | path | `string` | yes | Rachio person ID for the property owner. |
