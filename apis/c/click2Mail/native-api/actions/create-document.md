# Create Document with Click2Mail

Creates a new document in Click2Mail.

## Endpoint

- **Method:** `POST`
- **Path:** `/molpro/documents`
- **Base URL:** `https://stage-rest.click2mail.com`
- **Official documentation:** [Create Document](https://developers.click2mail.com/reference/createdocument_1)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `documentName` | query | `string` | no | Document name as it will be stored in your account |
| `documentFormat` | query | `string` | yes | Document format |
| `documentClass` | query | `string` | yes | Document Class |
| `file` | body | `string` | no | — |
