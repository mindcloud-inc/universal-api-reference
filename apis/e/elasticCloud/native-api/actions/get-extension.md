# Get Extension with Elastic Cloud

Retrieves an extension from Elastic Cloud.

## Endpoint

- **Method:** `GET`
- **Path:** `/deployments/extensions/:extension_id`
- **Base URL:** `https://api.elastic-cloud.com/api/v1`
- **Official documentation:** [Get Extension](https://www.elastic.co/docs/api/doc/cloud/operation/operation-get-extension)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `extension_id` | path | `string` | yes | Identifier for the extension. |
| `include_deployments` | query | `boolean` | no | Include deployments that reference this extension. |
