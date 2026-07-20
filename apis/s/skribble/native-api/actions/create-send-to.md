# Create Send-To with Skribble

Creates a Send-To signing request in Skribble.

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
| `content` | body | `string` | yes | The base64 encoded PDF content. |
| `title` | body | `string` | no | The Send-To title. |
