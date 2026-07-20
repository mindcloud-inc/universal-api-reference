# FlowFast: Create Card

Creates a new card in FlowFast.

```
POST https://connect.mindcloud.co/v1/universal/flowFast/latest/actions/create-card
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a FlowFast `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/flowFast/latest/actions/create-card" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/flowFast/latest/actions/create-card', {
  method: 'POST',
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
| `boardId` | string | no |  |
| `columnId` | string | no |  |
| `laneId` | string | no |  |
| `title` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "archived": true,
      "boardId": 1,
      "id": 1,
      "title": "string",
      "uid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `archived` | boolean |  |
| `boardId` | number |  |
| `id` | number |  |
| `title` | string |  |
| `uid` | string |  |

## Native endpoint

Through the native FlowFast API, this operation is `POST /cards` (base URL `https://apps.flowfast.io/api/latest/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-card.md) for the provider-specific parameters and requirements.

