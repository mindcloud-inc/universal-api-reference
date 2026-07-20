# Delete URL Orb Allow List Entry with CircleCI

## Endpoint

- **Method:** `DELETE`
- **Path:** `/organization/:org_slug_or_id/url-orb-allow-list/:allow_list_entry_id`
- **Base URL:** `https://circleci.com/api/v2`
- **Official documentation:** [Delete URL Orb Allow List Entry](https://circleci.com/docs/api/v2/#tag/URL-Orb-Allow-List/operation/removeURLOrbAllowListEntry)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `allow_list_entry_id` | path | `string` | yes | The URL orb allow-list entry UUID. |
| `org_slug_or_id` | path | `string` | yes | The CircleCI organization slug or ID. |
