# Create Send-To with Skribble Sign

Creates a new Send-To request in Skribble Sign.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/sendto`
- **Base URL:** `https://api.skribble.com`
- **Official documentation:** [Create Send-To](https://api-doc.skribble.com/#1b649c7f-5bfa-4c8c-b9db-5eb7a71bdd6c)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `title` | body | `string` | no | The Send-To title. |
| `content` | body | `string` | yes | The base64 encoded PDF content. |
