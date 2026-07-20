# Create Template With Buttons with Gupshup

Creates a template with buttons in Gupshup.

## Endpoint

- **Method:** `POST`
- **Path:** `/wa/app/{app_id}/template`
- **Base URL:** `https://api.gupshup.io`
- **Official documentation:** [Create Template With Buttons](https://docs.gupshup.io/docs/template-button-list)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/x-www-form-urlencoded` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `app_id` | path | `string` | yes | Gupshup app ID. |
| `languageCode` | body | `string` | no | Valid language code for the template. |
| `content` | body | `string` | yes | Template body content. |
| `buttons` | body | `object` | no | Template button configuration. |
