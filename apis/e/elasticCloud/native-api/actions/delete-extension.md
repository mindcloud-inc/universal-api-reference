# Delete Extension with Elastic Cloud

Deletes an existing extension from Elastic Cloud.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/deployments/extensions/:extension_id`
- **Base URL:** `https://api.elastic-cloud.com/api/v1`
- **Official documentation:** [Delete Extension](https://www.elastic.co/docs/api/doc/cloud/operation/operation-delete-extension)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `extension_id` | path | `string` | yes | Identifier for the extension. |
