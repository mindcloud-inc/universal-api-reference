# Count Form Comments with Wufoo

Retrieves the comment count for a Wufoo form.

## Endpoint

- **Method:** `GET`
- **Path:** `/forms/:identifier/comments/count.json`
- **Base URL:** `https://{subdomain}.wufoo.com/api/v3`
- **Official documentation:** [Count Form Comments](https://wufoo.github.io/docs/#forms)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `identifier` | path | `string` | yes | The form hash or identifier whose comments to count. |
