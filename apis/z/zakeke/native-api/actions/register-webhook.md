# Register Webhook with Zakeke

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/webhook`
- **Base URL:** `https://api.zakeke.com`
- **Official documentation:** [Register Webhook](https://api-reference.zakeke.com/docs)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | body | `string` | yes | Webhook destination URL. |
