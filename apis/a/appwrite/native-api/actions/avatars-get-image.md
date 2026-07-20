# Get image from URL with Appwrite

Retrieves an image from a URL with Appwrite.

## Endpoint

- **Method:** `GET`
- **Path:** `/avatars/image`
- **Base URL:** `https://cloud.appwrite.io/v1`
- **Official documentation:** [Get image from URL](https://appwrite.io/docs/references/cloud/server-rest/avatars)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | query | `string` | yes | Image URL which you want to crop. |
| `width` | query | `number` | no | Resize preview image width, Pass an integer between 0 to 2000. Defaults to 400. |
| `height` | query | `number` | no | Resize preview image height, Pass an integer between 0 to 2000. Defaults to 400. |
