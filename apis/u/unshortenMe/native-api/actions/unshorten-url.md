# Unshorten URL with Unshorten.Me

Retrieves an unshortened destination URL from Unshorten.Me.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v2/unshorten`
- **Base URL:** `https://unshorten.me`
- **Official documentation:** [Unshorten URL](https://unshorten.me/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | query | `string` | yes | The shortened URL to resolve, such as a bit.ly or TinyURL link. |
