# Update a Document with SignalWire

Updates an existing document in SignalWire.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/datasphere/documents/{id}`
- **Base URL:** `https://mindcloud.signalwire.com/api`
- **Official documentation:** [Update a Document](https://signalwire.com/docs/apis/rest/documents/update-document)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Unique ID of a Document. |
| `tags[]` | body | `array<string>` | no | Document tags. |
