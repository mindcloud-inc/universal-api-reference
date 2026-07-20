# Create Snapshot with Crazy Egg

## Endpoint

- **Method:** `POST`
- **Path:** `/snapshots.json`
- **Base URL:** `https://app.crazyegg.com/api/v2`
- **Official documentation:** [Create Snapshot](https://support.crazyegg.com/knowledge-base/)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/x-www-form-urlencoded` |

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `snapshot[source_url]` | body | `string` | yes |
| `snapshot[name]` | body | `string` | yes |
| `snapshot[max_visits]` | body | `number` | no |
| `snapshot[expires_at]` | body | `number` | no |
| `snapshot[starts_at]` | body | `number` | no |
| `snapshot[description]` | body | `string` | no |
| `snapshot[url_matching_rules]` | body | `string` | no |
| `snapshot[sampling_ratio]` | body | `number` | no |
| `snapshot[device]` | body | `string` | no |
