# Create Duration with NeetoCal

Creates a new meeting duration in NeetoCal.

## Endpoint

- **Method:** `POST`
- **Path:** `/meetings/:meeting_sid/durations`
- **Base URL:** `https://{subdomain}.neetocal.com/api/external/v2`
- **Official documentation:** [Create Duration](https://apidocs.neetocal.com/api-reference/meeting-durations/create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `meeting_sid` | path | `string` | yes | The scheduling link SID. |
| `duration` | body | `number` | yes | Duration in minutes. |
