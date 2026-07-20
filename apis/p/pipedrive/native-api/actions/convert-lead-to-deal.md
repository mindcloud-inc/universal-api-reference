# Convert Lead To Deal with Pipedrive

Converts a lead to a deal in Pipedrive.

## Endpoint

- **Method:** `POST`
- **Path:** `v2/leads/:id/convert/deal`
- **Base URL:** `{api_domain}/api`
- **Official documentation:** [Convert Lead To Deal](https://developers.pipedrive.com/docs/api/v1/Leads)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Lead ID to convert into a deal. |
| `stage_id` | body | `number` | no | Optional stage ID where the created deal will be placed. |
| `pipeline_id` | body | `number` | no | Optional pipeline ID where the created deal will be placed. |
