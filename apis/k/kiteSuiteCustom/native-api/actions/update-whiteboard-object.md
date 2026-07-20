# Update Whiteboard Object with Kite Suite

## Endpoint

- **Method:** `PATCH`
- **Path:** `/api/v1/white-board/object/:id`
- **Base URL:** `https://api.kitesuite.com`
- **Official documentation:** [Update Whiteboard Object](https://api.kitesuite.com/swagger/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `body` | body | `object` | yes | Request body |
| `id` | path | `string` | yes | ID of the object to update. |
| `name` | body | `string` | yes | Updated name of the object. |
| `type` | body | `string` | yes | Updated type of the object. |
| `top` | body | `number` | yes | Updated top position of the object. |
| `left` | body | `number` | yes | Updated left position of the object. |
| `width` | body | `number` | yes | Updated width of the object. |
| `height` | body | `number` | yes | Updated height of the object. |
| `fill` | body | `string` | yes | Updated fill color of the object. |
| `textValue` | body | `string` | yes | Updated text value of the object. |
| `style` | body | `object` | yes | Updated style properties of the object. |
| `scaleX` | body | `number` | yes | Updated horizontal scaling factor. |
| `scaleY` | body | `number` | yes | Updated vertical scaling factor. |
| `textStyle` | body | `object` | yes | Updated text style properties of the object. |
| `startNode` | body | `string` | yes | Updated ID of the start node for node lines. |
| `endNode` | body | `string` | yes | Updated ID of the end node for node lines. |
| `path` | body | `string` | yes | Updated path data for custom shapes. |
| `angle` | body | `number` | yes | updated Angle of rotation for the object. |
