# Create postback with Rakuten Advertising

Creates a new postback in Rakuten Advertising.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/postback`
- **Base URL:** `https://api.linksynergy.com`
- **Official documentation:** [Create postback](https://developers.rakutenadvertising.com/documentation/en-US/affiliate_apis/postback)

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
| `sid` | body | `string` | yes | Rakuten publisher SID. |
| `url` | body | `string` | yes | URL that Rakuten calls for transaction postbacks. |
