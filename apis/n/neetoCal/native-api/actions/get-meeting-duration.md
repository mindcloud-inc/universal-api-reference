# Get Duration with NeetoCal

Retrieves a meeting duration from NeetoCal.

## Endpoint

- **Method:** `GET`
- **Path:** `/meetings/:meeting_sid/durations/:id`
- **Base URL:** `https://{subdomain}.neetocal.com/api/external/v2`
- **Official documentation:** [Get Duration](https://apidocs.neetocal.com/api-reference/meeting-durations/get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `meeting_sid` | path | `string` | yes | The scheduling link SID. |
| `id` | path | `string` | yes | The duration ID. |
