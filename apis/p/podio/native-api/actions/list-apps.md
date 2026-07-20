# List Apps with Podio

Retrieves a list of apps from Podio.

## Endpoint

- **Method:** `GET`
- **Path:** `/app/`
- **Base URL:** `https://api.podio.com`
- **Official documentation:** [List Apps](https://developers.podio.com/doc/applications/get-all-apps-5902728)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `text` | query | `string` | no | Search term matching app names, item names, or workspace names. |
| `limit` | query | `number` | no | The maximum number of apps to return. |
| `order` | query | `string` | no | The order to return the apps in. |
| `exclude_demo` | query | `boolean` | no | True if apps from the demo workspace should be excluded. |
| `exclude_app_ids` | query | `string` | no | Comma-separated list of app IDs to exclude from the returned list. Send multiple values as a string separated by `,`. |
| `referenceable_in_org` | query | `number` | no | Organization ID to filter apps by. |
| `right` | query | `string` | no | The right the user must have on the returned apps. |
| `target_space_id` | query | `number` | no | Preferred space ID to prioritize apps from. |
