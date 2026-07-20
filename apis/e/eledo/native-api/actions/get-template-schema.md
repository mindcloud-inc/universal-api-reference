# Get Template Schema with Eledo

Retrieves a template schema from Eledo.

## Endpoint

- **Method:** `GET`
- **Path:** `/Schema/:template_id/:template_version`
- **Base URL:** `https://eledo.online/api/RESTv1`
- **Official documentation:** [Get Template Schema](https://eledo.online/documentation/api_reference/schema)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `template_id` | path | `string` | yes | — |
| `template_version` | path | `number` | no | — |
| `schemaType` | query | `string` | no | Optional schema type. Eledo documents zapier as the available value. |
