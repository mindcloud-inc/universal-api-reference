# Add Objects to Whiteboard with Kite Suite

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/white-board/object`
- **Base URL:** `https://api.kitesuite.com`
- **Official documentation:** [Add Objects to Whiteboard](https://api.kitesuite.com/swagger/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `board` | body | `string` | yes | ID of the whiteboard. |
| `body` | body | `object` | yes | Request body |
| `type` | body | `string` | yes | Type of object. |
| `name` | body | `string` | yes | Name of the object. |
| `top` | body | `number` | yes | Top position of the object. |
| `left` | body | `number` | yes | Left position of the object. |
| `width` | body | `number` | yes | Width of the object. |
| `height` | body | `number` | yes | Height of the object. |
| `fill` | body | `string` | yes | Fill color of the object. |
| `angle` | body | `number` | yes | Angle of rotation for the object. |
| `path` | body | `string` | yes | Path data for custom shapes. |
| `startNode` | body | `string` | yes | ID of the start node for node lines. |
| `endNode` | body | `string` | yes | ID of the end node for node lines. |
| `textValue` | body | `string` | yes | Text value for text boxes and links. |
| `scaleX` | body | `number` | yes | Horizontal scaling factor. |
| `scaleY` | body | `number` | yes | Vertical scaling factor. |
| `style` | body | `object` | yes | Style properties for the object. |
| `textStyle` | body | `object` | yes | Text style properties for text boxes. |
| `imagePath` | body | `string` | yes | Path to the image for image objects. |
| `item` | body | `string` | yes | ID of the item for item objects. |
| `id` | body | `string` | yes | Unique ID for the object. |
