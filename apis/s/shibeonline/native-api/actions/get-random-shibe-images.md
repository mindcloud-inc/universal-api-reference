# Get Random Shibe Images with Shibe.online

## Endpoint

- **Method:** `GET`
- **Path:** `/api/shibes`
- **Base URL:** `https://shibe.online`
- **Official documentation:** [Get Random Shibe Images](https://shibe.online/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `count` | query | `number` | no | Number of images to return (1 through 100). Maximum length: 100. |
| `urls` | query | `boolean` | no | When true, return image URLs; when false, the provider can return non-URL values. |
| `httpsUrls` | query | `boolean` | no | When returning URLs, request HTTPS image URLs. |
