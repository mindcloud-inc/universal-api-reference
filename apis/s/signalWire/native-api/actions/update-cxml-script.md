# Update cXML Script with SignalWire

Updates an existing cXML script in SignalWire.

## Endpoint

- **Method:** `PUT`
- **Path:** `/fabric/resources/cxml_scripts/{id}`
- **Base URL:** `https://mindcloud.signalwire.com/api`
- **Official documentation:** [Update cXML Script](https://signalwire.com/docs/apis/rest/cxml-scripts/update-cxml-script)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Unique ID of a cXML Script. |
| `display_name` | body | `string` | no | Display name of the cXML Script |
| `contents` | body | `string` | no | The cXML script contents |
| `status_callback_url` | body | `string` | no | URL to send status callbacks to |
| `status_callback_method` | body | `string` | no | HTTP method to use for status callbacks |
