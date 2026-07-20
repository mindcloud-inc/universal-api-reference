# Unblock Url with Browserless

Retrieves page content from blocked sites in Browserless.

## Endpoint

- **Method:** `POST`
- **Path:** `/unblock`
- **Base URL:** `https://production-sfo.browserless.io`
- **Official documentation:** [Unblock Url](https://docs.browserless.io/rest-apis/unblock)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | body | `string` | yes | The URL of the site to unblock. |
| `content` | body | `boolean` | no | Whether to return HTML content in the unblock response. |
| `cookies` | body | `boolean` | no | Whether to return cookies in the unblock response. |
| `screenshot` | body | `boolean` | no | Whether to return a full-page screenshot in the unblock response. |
| `browserWSEndpoint` | body | `boolean` | no | Whether to keep the browser alive and return a browserWSEndpoint for reconnects. |
