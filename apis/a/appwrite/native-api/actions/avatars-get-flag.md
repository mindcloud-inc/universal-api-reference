# Get country flag with Appwrite

Retrieves a country flag from Appwrite.

## Endpoint

- **Method:** `GET`
- **Path:** `/avatars/flags/{code}`
- **Base URL:** `https://cloud.appwrite.io/v1`
- **Official documentation:** [Get country flag](https://appwrite.io/docs/references/cloud/server-rest/avatars)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `code` | path | `file` | yes | Country Code. ISO Alpha-2 country code format. |
| `width` | query | `number` | no | Image width. Pass an integer between 0 to 2000. Defaults to 100. |
| `height` | query | `number` | no | Image height. Pass an integer between 0 to 2000. Defaults to 100. |
| `quality` | query | `number` | no | Image quality. Pass an integer between 0 to 100. Defaults to keep existing image quality. |
