# Delete Templates By Code with Zakeke

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/designs/templates/code/:templateCode/delete`
- **Base URL:** `https://api.zakeke.com`
- **Official documentation:** [Delete Templates By Code](https://docs.zakeke.com/docs/API/designs-API#12-delete-templates-by-code)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `templateCode` | path | `string` | yes | Template code to delete across products. |
