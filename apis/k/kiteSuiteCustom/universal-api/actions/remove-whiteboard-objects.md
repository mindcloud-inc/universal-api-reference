# Kite Suite: remove Whiteboard Objects



```
POST https://connect.mindcloud.co/v1/universal/kiteSuiteCustom/latest/actions/remove-whiteboard-objects
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Kite Suite `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/kiteSuiteCustom/latest/actions/remove-whiteboard-objects" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "board": "string",
  "body": {},
  "objects[]": [
    "string"
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/kiteSuiteCustom/latest/actions/remove-whiteboard-objects', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "board": "string",
    "body": {},
    "objects[]": ["string"]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `board` | string | yes | ID of the whiteboard containing the objects. |
| `body` | object | yes | Request body |
| `objects[]` | array | yes | Array of object IDs to delete. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string",
      "statusCode": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string |  |
| `statusCode` | number |  |

## Native endpoint

Through the native Kite Suite API, this operation is `POST /api/v1/white-board/object/remove` (base URL `https://api.kitesuite.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/remove-whiteboard-objects.md) for the provider-specific parameters and requirements.

