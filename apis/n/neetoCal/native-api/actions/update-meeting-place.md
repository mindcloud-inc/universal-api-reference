# Update Place with NeetoCal

Updates an existing meeting place in NeetoCal.

## Endpoint

- **Method:** `PUT`
- **Path:** `/meetings/:meeting_sid/spots/:id`
- **Base URL:** `https://{subdomain}.neetocal.com/api/external/v2`
- **Official documentation:** [Update Place](https://apidocs.neetocal.com/api-reference/meeting-places/update)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `meeting_sid` | path | `string` | yes | The scheduling link SID. |
| `id` | path | `string` | yes | The meeting place ID. |
| `spot` | body | `string` | yes | The meeting place type. |
| `spot_custom_text` | body | `string` | no | Custom text for a custom meeting place. |
