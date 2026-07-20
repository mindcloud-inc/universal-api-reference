# Create cXML Script with SignalWire

Creates a new cXML script in SignalWire.

## Endpoint

- **Method:** `POST`
- **Path:** `/fabric/resources/cxml_scripts`
- **Base URL:** `https://mindcloud.signalwire.com/api`
- **Official documentation:** [Create cXML Script](https://signalwire.com/docs/apis/rest/cxml-scripts/create-cxml-script)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `display_name` | body | `string` | yes | Display name of the cXML Script |
| `contents` | body | `string` | yes | The cXML script contents |
| `status_callback_url` | body | `string` | no | URL to send status callbacks to |
| `status_callback_method` | body | `string` | no | HTTP method to use for status callbacks |
