# Update Snapshot with Crazy Egg

## Endpoint

- **Method:** `PUT`
- **Path:** `/snapshot/:id.json`
- **Base URL:** `https://app.crazyegg.com/api/v2`
- **Official documentation:** [Update Snapshot](https://support.crazyegg.com/knowledge-base/)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/x-www-form-urlencoded` |

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id` | path | `string` | yes |
| `snapshot[source_url]` | body | `string` | no |
| `snapshot[name]` | body | `string` | no |
| `snapshot[max_visits]` | body | `number` | no |
| `snapshot[expires_at]` | body | `number` | no |
| `snapshot[starts_at]` | body | `number` | no |
| `snapshot[description]` | body | `string` | no |
| `snapshot[url_matching_rules]` | body | `string` | no |
| `snapshot[sampling_ratio]` | body | `number` | no |
| `snapshot[device]` | body | `string` | no |
