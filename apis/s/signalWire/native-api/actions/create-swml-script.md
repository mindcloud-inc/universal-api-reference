# Create SWML Script with SignalWire

Creates a new SWML script in SignalWire.

## Endpoint

- **Method:** `POST`
- **Path:** `/fabric/resources/swml_scripts`
- **Base URL:** `https://mindcloud.signalwire.com/api`
- **Official documentation:** [Create SWML Script](https://signalwire.com/docs/apis/rest/swml-scripts/create-swml-script)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Display name of the SWML Script |
| `contents` | body | `string` | yes | The contents of the SWML script. |
| `status_callback_url` | body | `string` | no | URL to send status callbacks to |
