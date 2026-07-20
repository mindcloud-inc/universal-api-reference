# Hey Reach: Create Empty List

Creates an empty lead or company list in Hey Reach.

```
POST https://connect.mindcloud.co/v1/universal/heyReach/latest/actions/create-empty-list
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Hey Reach `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/heyReach/latest/actions/create-empty-list" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen",
  "type": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/heyReach/latest/actions/create-empty-list', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen",
    "type": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes |  |
| `type` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "campaigns": "string",
      "count": 1,
      "creationTime": "string",
      "id": 1,
      "isDeleted": true,
      "listType": "string",
      "name": "Ava Chen",
      "search": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `campaigns` | string |  |
| `count` | number |  |
| `creationTime` | string |  |
| `id` | number |  |
| `isDeleted` | boolean |  |
| `listType` | string |  |
| `name` | string |  |
| `search` | string |  |
| `status` | string |  |

## Native endpoint

Through the native Hey Reach API, this operation is `POST /api/public/list/CreateEmptyList` (base URL `https://api.heyreach.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-empty-list.md) for the provider-specific parameters and requirements.

