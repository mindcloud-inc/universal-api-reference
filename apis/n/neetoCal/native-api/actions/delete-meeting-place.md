# Delete Place with NeetoCal

Deletes an existing meeting place from NeetoCal.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/meetings/:meeting_sid/spots/:id`
- **Base URL:** `https://{subdomain}.neetocal.com/api/external/v2`
- **Official documentation:** [Delete Place](https://apidocs.neetocal.com/api-reference/meeting-places/delete)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `meeting_sid` | path | `string` | yes | The scheduling link SID. |
| `id` | path | `string` | yes | The meeting place ID. |
