# Get Tag with Discourse

Retrieves a specific tag from Discourse.

## Endpoint

- **Method:** `GET`
- **Path:** `/tag/:name.json`
- **Base URL:** `https://mindcloud.discourse.group`
- **Official documentation:** [Get Tag](https://docs.discourse.org/#tag/Tags/operation/getTag)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | path | `string` | yes | Tag slug or name. |
