# WEBLUCY: Update Subscriber List

Updates an existing subscriber list in WEBLUCY.

```
PUT https://connect.mindcloud.co/v1/universal/wEBLUCY/latest/actions/update-subscriber-list
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a WEBLUCY `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/wEBLUCY/latest/actions/update-subscriber-list" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/wEBLUCY/latest/actions/update-subscriber-list', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | The subscriber list ID. |

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

Through the native WEBLUCY API, this operation is `PUT /subscriber-lists/{id}` (base URL `https://apps.weblucy.com/api/site`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-subscriber-list.md) for the provider-specific parameters and requirements.

