# Delete Duration with NeetoCal

Deletes an existing meeting duration from NeetoCal.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/meetings/:meeting_sid/durations/:id`
- **Base URL:** `https://{subdomain}.neetocal.com/api/external/v2`
- **Official documentation:** [Delete Duration](https://apidocs.neetocal.com/api-reference/meeting-durations/delete)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `meeting_sid` | path | `string` | yes | The scheduling link SID. |
| `id` | path | `string` | yes | The duration ID. |
