# Update Scheduling Link with NeetoCal

Updates an existing scheduling link in NeetoCal.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/meetings/:meeting_sid`
- **Base URL:** `https://{subdomain}.neetocal.com/api/external/v2`
- **Official documentation:** [Update Scheduling Link](https://apidocs.neetocal.com/api-reference/scheduling-links/update)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `meeting_sid` | path | `string` | yes | The scheduling link SID. |
| `hosts[]` | body | `array<string>` | yes | Host emails for the scheduling link. |
| `name` | body | `string` | no | Updated display name for the scheduling link. |
