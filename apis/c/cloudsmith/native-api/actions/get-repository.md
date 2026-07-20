# Get Repository with Cloudsmith

## Endpoint

- **Method:** `GET`
- **Path:** `/repos/:owner/:identifier/`
- **Base URL:** `https://api.cloudsmith.io`
- **Official documentation:** [Get Repository](https://help.cloudsmith.io/reference/repos_read)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `owner` | path | `string` | yes | Repository owner namespace slug. |
| `identifier` | path | `string` | yes | Repository identifier or slug. |
