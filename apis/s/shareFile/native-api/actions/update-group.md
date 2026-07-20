# Update Group with ShareFile

## Endpoint

- **Method:** `PATCH`
- **Path:** `/Groups({{id}})`
- **Base URL:** `https://{subdomain}.{apicp}/sf/v3`
- **Official documentation:** [Update Group](https://api.sharefile.com/html/docs/Groups.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The ShareFile group identifier to update. |
| `Group` | body | `object` | yes | The ShareFile group object to update. |
