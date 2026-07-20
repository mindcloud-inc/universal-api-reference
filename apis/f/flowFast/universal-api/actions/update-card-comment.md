# FlowFast: Update Card Comment

Updates an existing card comment in FlowFast.

```
PUT https://connect.mindcloud.co/v1/universal/flowFast/latest/actions/update-card-comment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a FlowFast `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/flowFast/latest/actions/update-card-comment" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/flowFast/latest/actions/update-card-comment', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `cardId` | string | no |  |
| `commentId` | string | no |  |
| `text` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "cardId": 1,
      "id": 1,
      "text": "string",
      "uid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `cardId` | number |  |
| `id` | number |  |
| `text` | string |  |
| `uid` | string |  |

## Native endpoint

Through the native FlowFast API, this operation is `PATCH /cards/:cardId/comments/:commentId` (base URL `https://apps.flowfast.io/api/latest/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-card-comment.md) for the provider-specific parameters and requirements.

