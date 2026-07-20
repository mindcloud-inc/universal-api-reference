# Create Template with Gupshup

Creates a template in Gupshup.

## Endpoint

- **Method:** `POST`
- **Path:** `/wa/app/{app_id}/template`
- **Base URL:** `https://api.gupshup.io`
- **Official documentation:** [Create Template](https://docs.gupshup.io/docs/create-template)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/x-www-form-urlencoded` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `app_id` | path | `string` | yes | Gupshup app ID. |
| `example` | body | `string` | no | Template body example values when variables are used. |
| `footer` | body | `string` | no | Optional template footer text. |
| `vertical` | body | `string` | no | Template vertical or use case label. |
| `languageCode` | body | `string` | yes | Valid language code for the template. |
| `content` | body | `string` | yes | Template body content. |
| `category` | body | `string` | yes | Template category. |
| `elementName` | body | `string` | yes | Template name/element name. |
