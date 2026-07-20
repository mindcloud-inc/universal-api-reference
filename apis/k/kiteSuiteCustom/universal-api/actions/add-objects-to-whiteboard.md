# Kite Suite: Add Objects to Whiteboard



```
POST https://connect.mindcloud.co/v1/universal/kiteSuiteCustom/latest/actions/add-objects-to-whiteboard
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Kite Suite `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/kiteSuiteCustom/latest/actions/add-objects-to-whiteboard" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "board": "string",
  "body": {},
  "type": "string",
  "name": "Ava Chen",
  "top": 1,
  "left": 1,
  "width": 1,
  "height": 1,
  "fill": "string",
  "angle": 1,
  "path": "string",
  "startNode": "string",
  "endNode": "string",
  "textValue": "string",
  "scaleX": 1,
  "scaleY": 1,
  "style": {},
  "textStyle": {},
  "imagePath": "string",
  "item": "string",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/kiteSuiteCustom/latest/actions/add-objects-to-whiteboard', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "board": "string",
    "body": {},
    "type": "string",
    "name": "Ava Chen",
    "top": 1,
    "left": 1,
    "width": 1,
    "height": 1,
    "fill": "string",
    "angle": 1,
    "path": "string",
    "startNode": "string",
    "endNode": "string",
    "textValue": "string",
    "scaleX": 1,
    "scaleY": 1,
    "style": {},
    "textStyle": {},
    "imagePath": "string",
    "item": "string",
    "id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `board` | string | yes | ID of the whiteboard. |
| `body` | object | yes | Request body |
| `type` | string | yes | Type of object. |
| `name` | string | yes | Name of the object. |
| `top` | number | yes | Top position of the object. |
| `left` | number | yes | Left position of the object. |
| `width` | number | yes | Width of the object. |
| `height` | number | yes | Height of the object. |
| `fill` | string | yes | Fill color of the object. |
| `angle` | number | yes | Angle of rotation for the object. |
| `path` | string | yes | Path data for custom shapes. |
| `startNode` | string | yes | ID of the start node for node lines. |
| `endNode` | string | yes | ID of the end node for node lines. |
| `textValue` | string | yes | Text value for text boxes and links. |
| `scaleX` | number | yes | Horizontal scaling factor. |
| `scaleY` | number | yes | Vertical scaling factor. |
| `style` | object | yes | Style properties for the object. |
| `textStyle` | object | yes | Text style properties for text boxes. |
| `imagePath` | string | yes | Path to the image for image objects. |
| `item` | string | yes | ID of the item for item objects. |
| `id` | string | yes | Unique ID for the object. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "value": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `value` | object | Added whiteboard object. |

## Native endpoint

Through the native Kite Suite API, this operation is `POST /api/v1/white-board/object` (base URL `https://api.kitesuite.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-objects-to-whiteboard.md) for the provider-specific parameters and requirements.

