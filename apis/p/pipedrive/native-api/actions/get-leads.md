# Get Leads with Pipedrive

Retrieves leads from Pipedrive.

## Endpoint

- **Method:** `GET`
- **Path:** `v1/leads`
- **Base URL:** `{api_domain}/api`
- **Official documentation:** [Get Leads](https://developers.pipedrive.com/docs/api/v1/Leads)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `limit` | query | `number` | no | Max number of leads to return. |
| `start` | query | `number` | no | Offset for lead pagination. |
| `updated_since` | query | `string` | no | Return leads updated after this timestamp. |
| `sort` | query | `string` | no | Sort leads by a timestamp field and direction. |
| `owner_id` | query | `number` | no | Filter leads by owner user ID. |
