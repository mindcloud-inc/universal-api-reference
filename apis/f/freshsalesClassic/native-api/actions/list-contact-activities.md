# List Contact Activities with Freshsales Classic

Retrieves activities for a contact from Freshsales Classic.

## Endpoint

- **Method:** `GET`
- **Path:** `/contacts/:id/activities`
- **Base URL:** `https://{bundleAlias}/api`
- **Official documentation:** [List Contact Activities](https://developers.freshworks.com/crm/api/#list_all_contact_activities)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | Freshsales contact id to inspect for timeline activities. |
| `include` | query | `string` | no | Optional embedded resources, such as user. |
| `limit` | query | `number` | no | Maximum number of activities to return. |
