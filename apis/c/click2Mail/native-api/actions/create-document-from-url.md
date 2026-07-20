# Create Document From URL with Click2Mail

Creates a document in Click2Mail from a URL.

## Endpoint

- **Method:** `POST`
- **Path:** `/molpro/documents/url`
- **Base URL:** `https://stage-rest.click2mail.com`
- **Official documentation:** [Create Document From URL](https://developers.click2mail.com/reference/createdocumentfromurl)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `documentName` | query | `string` | no | Document name as it will be stored in your account |
| `documentFormat` | query | `string` | yes | document Format |
| `documentClass` | query | `string` | yes | Document Class |
| `url` | query | `string` | yes | Document url |
