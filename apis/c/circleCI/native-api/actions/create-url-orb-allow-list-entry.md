# Create URL Orb Allow List Entry with CircleCI

## Endpoint

- **Method:** `POST`
- **Path:** `/organization/:org_slug_or_id/url-orb-allow-list`
- **Base URL:** `https://circleci.com/api/v2`
- **Official documentation:** [Create URL Orb Allow List Entry](https://circleci.com/docs/api/v2/#tag/URL-Orb-Allow-List/operation/createURLOrbAllowListEntry)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `auth` | body | `string` | yes | The auth mode for fetching matching URL orbs. |
| `name` | body | `string` | yes | The allow-list entry name. |
| `org_slug_or_id` | path | `string` | yes | The CircleCI organization slug or ID. |
| `prefix` | body | `string` | yes | The URL prefix to allow. |
