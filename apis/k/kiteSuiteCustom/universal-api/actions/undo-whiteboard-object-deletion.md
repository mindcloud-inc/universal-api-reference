# Kite Suite: Undo Whiteboard Object Deletion



```
PUT https://connect.mindcloud.co/v1/universal/kiteSuiteCustom/latest/actions/undo-whiteboard-object-deletion
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Kite Suite `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/kiteSuiteCustom/latest/actions/undo-whiteboard-object-deletion" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "_id": "string",
  "body": {},
  "nodes[]": [
    "string"
  ],
  "index": 1,
  "type": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/kiteSuiteCustom/latest/actions/undo-whiteboard-object-deletion', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "_id": "string",
    "body": {},
    "nodes[]": ["string"],
    "index": 1,
    "type": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `_id` | string | yes | ID of the object to restore. |
| `body` | object | yes | Request body |
| `nodes[]` | array | yes | Array of node objects to restore. |
| `index` | number | yes | Position of the restored object in the whiteboard's object list. |
| `type` | string | yes | Type of object being restored. |

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
| `value` | object | Restored whiteboard object. |

## Native endpoint

Through the native Kite Suite API, this operation is `PATCH /api/v1/white-board/object/undo-redo` (base URL `https://api.kitesuite.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/undo-whiteboard-object-deletion.md) for the provider-specific parameters and requirements.

