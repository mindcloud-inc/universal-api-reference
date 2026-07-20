# Create Place with NeetoCal

Creates a new meeting place in NeetoCal.

## Endpoint

- **Method:** `POST`
- **Path:** `/meetings/:meeting_sid/spots`
- **Base URL:** `https://{subdomain}.neetocal.com/api/external/v2`
- **Official documentation:** [Create Place](https://apidocs.neetocal.com/api-reference/meeting-places/create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `meeting_sid` | path | `string` | yes | The scheduling link SID. |
| `spot` | body | `string` | yes | The meeting place type. |
| `spot_custom_text` | body | `string` | no | Custom text for a custom meeting place. |
