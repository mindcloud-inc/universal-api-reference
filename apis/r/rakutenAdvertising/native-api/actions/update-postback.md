# Update postback with Rakuten Advertising

Updates an existing postback in Rakuten Advertising.

## Endpoint

- **Method:** `PUT`
- **Path:** `/v1/postback/{sid}`
- **Base URL:** `https://api.linksynergy.com`
- **Official documentation:** [Update postback](https://developers.rakutenadvertising.com/documentation/en-US/affiliate_apis/postback)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `is_active` | body | `boolean` | yes | Whether the postback configuration is active. |
| `sid` | path | `string` | yes | Rakuten publisher SID. |
| `url` | body | `string` | yes | URL that Rakuten calls for transaction postbacks. |
