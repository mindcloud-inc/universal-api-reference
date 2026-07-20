# Update Duration with NeetoCal

Updates an existing meeting duration in NeetoCal.

## Endpoint

- **Method:** `PUT`
- **Path:** `/meetings/:meeting_sid/durations/:id`
- **Base URL:** `https://{subdomain}.neetocal.com/api/external/v2`
- **Official documentation:** [Update Duration](https://apidocs.neetocal.com/api-reference/meeting-durations/update)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `meeting_sid` | path | `string` | yes | The scheduling link SID. |
| `id` | path | `string` | yes | The duration ID. |
| `duration` | body | `number` | yes | Updated duration in minutes. |
