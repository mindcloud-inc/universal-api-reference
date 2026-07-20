# Get Signed Asset URL with Storyblok

Retrieves a signed URL for a private Storyblok asset.

## Endpoint

- **Method:** `GET`
- **Path:** `/assets/me`
- **Base URL:** `https://api.storyblok.com/v2/cdn`
- **Official documentation:** [Get Signed Asset URL](https://www.storyblok.com/docs/api/content-delivery/v2/assets/retrieve-signed-url)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `filename` | query | `string` | yes | The Storyblok asset URL to sign. |
