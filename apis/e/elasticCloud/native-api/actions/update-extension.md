# Update Extension with Elastic Cloud

Updates an existing extension in Elastic Cloud.

## Endpoint

- **Method:** `POST`
- **Path:** `/deployments/extensions/:extension_id`
- **Base URL:** `https://api.elastic-cloud.com/api/v1`
- **Official documentation:** [Update Extension](https://www.elastic.co/docs/api/doc/cloud/operation/operation-update-extension)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `body` | body | `object` | yes | The extension update data. |
| `extension_id` | path | `string` | yes | Identifier for the extension. |
