# Generate Image Or Video with Bannerbite

Creates an image or video render job in Bannerbite.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/render`
- **Base URL:** `https://api.bannerbite.com`
- **Official documentation:** [Generate Image Or Video](https://developer.bannerbite.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `audio` | body | `object` | no | Optional audio object containing url and inPoint. |
| `email` | body | `string` | no | Optional email address that receives the finished render. |
| `scene` | body | `number` | no | Required when type is image. Selects which scene to render. |
| `sceneData` | body | `list<object>` | yes | Array of scene variable objects to inject into the selected bite. Send each object with provider keys such as name, value, color, width, height, inPoint, outPoint, visibility, and position when applicable. |
| `type` | body | `string` | yes | Render type. Bannerbite documents image, video, and overlay. Accepted values: `0`, `1`, `2`. |
| `uid` | body | `string` | yes | The bite ID or bite access token used for the render request. |
| `webhook` | body | `string` | no | Optional webhook URL for render status notifications. |
