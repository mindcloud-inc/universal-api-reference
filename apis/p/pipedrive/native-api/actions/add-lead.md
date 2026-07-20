# Add Lead with Pipedrive

Creates a new lead in Pipedrive.

## Endpoint

- **Method:** `POST`
- **Path:** `v1/leads`
- **Base URL:** `{api_domain}/api`
- **Official documentation:** [Add Lead](https://developers.pipedrive.com/docs/api/v1/Leads)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `title` | body | `string` | yes | Lead title. |
| `person_id` | body | `number` | no | Person ID to link to the lead. |
| `organization_id` | body | `number` | no | Organization ID to link to the lead. |
