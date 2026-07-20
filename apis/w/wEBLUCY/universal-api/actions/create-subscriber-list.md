# WEBLUCY: Create Subscriber List

Creates a new subscriber list in WEBLUCY.

```
POST https://connect.mindcloud.co/v1/universal/wEBLUCY/latest/actions/create-subscriber-list
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a WEBLUCY `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/wEBLUCY/latest/actions/create-subscriber-list" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/wEBLUCY/latest/actions/create-subscriber-list', {
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



## Response

```json
{
  "success": true,
  "data": [
    {
      "clicks": 1,
      "created": 1,
      "id": 1,
      "name": "Ava Chen",
      "opens": 1,
      "subscribers": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `clicks` | number |  |
| `created` | number |  |
| `id` | number |  |
| `name` | string |  |
| `opens` | number |  |
| `subscribers` | number |  |

## Native endpoint

Through the native WEBLUCY API, this operation is `POST /subscriber-lists` (base URL `https://apps.weblucy.com/api/site`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-subscriber-list.md) for the provider-specific parameters and requirements.

