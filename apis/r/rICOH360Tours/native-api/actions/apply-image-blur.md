# Apply Image Blur with RICOH360 Tours

## Endpoint

- **Method:** `POST`
- **Path:** `/graphql`
- **Base URL:** `https://bbomwcm27nhalfwjvwzy6qbrim.appsync-api.us-west-2.amazonaws.com`
- **Official documentation:** [Apply Image Blur](https://help.ricoh360.com/hc/en-us/articles/4404305780371--7-29-2021-Blur)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `bucket` | query | `string` | no | Mask asset bucket. |
| `key` | query | `string` | no | Mask asset object key. |
| `mimeType` | query | `string` | no | Mask asset MIME type. |
| `radius` | query | `string` | no | Blur radius. |
| `region` | query | `string` | no | Mask asset region. |
| `roomId` | query | `string` | no | Room ID to blur. |
| `teamId` | query | `string` | no | Team ID that owns the room. |
