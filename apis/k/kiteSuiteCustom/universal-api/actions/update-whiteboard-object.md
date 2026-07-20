# Kite Suite: Update Whiteboard Object



```
PUT https://connect.mindcloud.co/v1/universal/kiteSuiteCustom/latest/actions/update-whiteboard-object
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Kite Suite `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/kiteSuiteCustom/latest/actions/update-whiteboard-object" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "body": {},
  "id": "string",
  "name": "Ava Chen",
  "type": "string",
  "top": 1,
  "left": 1,
  "width": 1,
  "height": 1,
  "fill": "string",
  "textValue": "string",
  "style": {},
  "scaleX": 1,
  "scaleY": 1,
  "textStyle": {},
  "startNode": "string",
  "endNode": "string",
  "path": "string",
  "angle": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/kiteSuiteCustom/latest/actions/update-whiteboard-object', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "body": {},
    "id": "string",
    "name": "Ava Chen",
    "type": "string",
    "top": 1,
    "left": 1,
    "width": 1,
    "height": 1,
    "fill": "string",
    "textValue": "string",
    "style": {},
    "scaleX": 1,
    "scaleY": 1,
    "textStyle": {},
    "startNode": "string",
    "endNode": "string",
    "path": "string",
    "angle": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `body` | object | yes | Request body |
| `id` | string | yes | ID of the object to update. |
| `name` | string | yes | Updated name of the object. |
| `type` | string | yes | Updated type of the object. |
| `top` | number | yes | Updated top position of the object. |
| `left` | number | yes | Updated left position of the object. |
| `width` | number | yes | Updated width of the object. |
| `height` | number | yes | Updated height of the object. |
| `fill` | string | yes | Updated fill color of the object. |
| `textValue` | string | yes | Updated text value of the object. |
| `style` | object | yes | Updated style properties of the object. |
| `scaleX` | number | yes | Updated horizontal scaling factor. |
| `scaleY` | number | yes | Updated vertical scaling factor. |
| `textStyle` | object | yes | Updated text style properties of the object. |
| `startNode` | string | yes | Updated ID of the start node for node lines. |
| `endNode` | string | yes | Updated ID of the end node for node lines. |
| `path` | string | yes | Updated path data for custom shapes. |
| `angle` | number | yes | updated Angle of rotation for the object. |

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
| `value` | object | Updated whiteboard object. |

## Native endpoint

Through the native Kite Suite API, this operation is `PATCH /api/v1/white-board/object/:id` (base URL `https://api.kitesuite.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-whiteboard-object.md) for the provider-specific parameters and requirements.

