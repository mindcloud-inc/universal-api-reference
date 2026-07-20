# zipBoard: Update Response

Updates an existing response in zipBoard.

```
PUT https://connect.mindcloud.co/v1/universal/zipBoard/latest/actions/update-response
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a zipBoard `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/zipBoard/latest/actions/update-response" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string",
  "reply": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/zipBoard/latest/actions/update-response', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string",
    "reply": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes |  |
| `mentionedIds[]` | array<string> | no |  |
| `reply` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "reply": "string",
      "taskid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string | Response identifier. |
| `reply` | string | Response body. |
| `taskid` | string | Task identifier. |

## Native endpoint

Through the native zipBoard API, this operation is `PUT /issues/responses/:id` (base URL `https://app.zipboard.co/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-response.md) for the provider-specific parameters and requirements.

