# Update SWML Script with SignalWire

Updates an existing SWML script in SignalWire.

## Endpoint

- **Method:** `PUT`
- **Path:** `/fabric/resources/swml_scripts/{id}`
- **Base URL:** `https://mindcloud.signalwire.com/api`
- **Official documentation:** [Update SWML Script](https://signalwire.com/docs/apis/rest/swml-scripts/update-swml-script)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Unique ID of a SWML Script. |
| `display_name` | body | `string` | no | Display name of the SWML Script |
| `contents` | body | `string` | no | The contents of the SWML script. |
| `status_callback_url` | body | `string` | no | URL to send status callbacks to |
