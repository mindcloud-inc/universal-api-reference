# Merge Document with Click2Mail

Creates a merged document in Click2Mail.

## Endpoint

- **Method:** `POST`
- **Path:** `/molpro/documents/merge`
- **Base URL:** `https://stage-rest.click2mail.com`
- **Official documentation:** [Merge Document](https://developers.click2mail.com/reference/mergedocument)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `documentName` | query | `string` | yes | Document name as it will be stored in your account |
| `documentIdlist[]` | body | `array<number>` | no | — |
