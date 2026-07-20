# Get Deal with Pipedrive

Retrieves a deal from Pipedrive.

## Endpoint

- **Method:** `GET`
- **Path:** `v2/deals/:id`
- **Base URL:** `{api_domain}/api`
- **Official documentation:** [Get Deal](https://developers.pipedrive.com/docs/api/v1/Deals#getDeal)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `custom_fields` | query | `string` | no | Comma-separated custom field hashes to include. |
| `id` | path | `number` | yes | Unique ID of the deal. |
| `include_fields` | query | `string` | no | Comma-separated additional fields to include. |
