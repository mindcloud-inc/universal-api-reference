# Get Organization with Pipedrive

Retrieves an organization from Pipedrive.

## Endpoint

- **Method:** `GET`
- **Path:** `v2/organizations/:id`
- **Base URL:** `{api_domain}/api`
- **Official documentation:** [Get Organization](https://developers.pipedrive.com/docs/api/v1/Organizations#getOrganization)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | Unique ID of the organization. |
| `include_fields` | query | `string` | no | Comma-separated additional fields to include. |
| `custom_fields` | query | `string` | no | Comma-separated custom field keys to include. |
