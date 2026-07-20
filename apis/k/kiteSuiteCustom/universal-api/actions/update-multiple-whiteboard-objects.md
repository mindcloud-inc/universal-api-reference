# Kite Suite: Update Multiple Whiteboard Objects



```
PUT https://connect.mindcloud.co/v1/universal/kiteSuiteCustom/latest/actions/update-multiple-whiteboard-objects
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Kite Suite `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/kiteSuiteCustom/latest/actions/update-multiple-whiteboard-objects" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "body": {},
  "objects[]": [
    "string"
  ],
  "isGroup": true
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/kiteSuiteCustom/latest/actions/update-multiple-whiteboard-objects', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "body": {},
    "objects[]": ["string"],
    "isGroup": true
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `body` | object | yes | Request body |
| `objects[]` | array | yes | Array of objects to update. |
| `isGroup` | boolean | yes | Group status of the objects. |

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

Through the native Kite Suite API, this operation is `POST /api/v1/white-board/object/multiple` (base URL `https://api.kitesuite.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-multiple-whiteboard-objects.md) for the provider-specific parameters and requirements.

