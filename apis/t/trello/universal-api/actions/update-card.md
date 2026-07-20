# Trello: Update Card

Updates an existing card in Trello.

```
PUT https://connect.mindcloud.co/v1/universal/trello/latest/actions/update-card
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Trello `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/trello/latest/actions/update-card" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/trello/latest/actions/update-card', {
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
| `desc` | string | no | Optional card description. |
| `id` | string | yes | Card identifier. |
| `idList` | string | no | Optional destination list ID for moving card. |
| `name` | string | no | Optional new card title. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "closed": true,
      "desc": "string",
      "id": "string",
      "idBoard": "string",
      "idList": "string",
      "name": "Ava Chen",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `closed` | boolean |  |
| `desc` | string |  |
| `id` | string |  |
| `idBoard` | string |  |
| `idList` | string |  |
| `name` | string |  |
| `url` | string |  |

## Native endpoint

Through the native Trello API, this operation is `PUT cards/:id` (base URL `https://api.trello.com/1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-card.md) for the provider-specific parameters and requirements.

