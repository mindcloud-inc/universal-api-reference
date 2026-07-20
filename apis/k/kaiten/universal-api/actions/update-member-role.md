# Kaiten: Update Member Role

Updates a card member role in Kaiten.

```
PUT https://connect.mindcloud.co/v1/universal/kaiten/latest/actions/update-member-role
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Kaiten `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/kaiten/latest/actions/update-member-role" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "cardId": 1,
  "id": 1,
  "type": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/kaiten/latest/actions/update-member-role', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "cardId": 1,
    "id": 1,
    "type": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `cardId` | number | yes | The Kaiten card ID. |
| `id` | number | yes | The Kaiten member user ID. |
| `type` | number | yes | The numeric member role type. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "card_id": 1,
      "created": "string",
      "type": 1,
      "updated": "string",
      "user_id": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `card_id` | number |  |
| `created` | string |  |
| `type` | number |  |
| `updated` | string |  |
| `user_id` | number |  |

## Native endpoint

Through the native Kaiten API, this operation is `PATCH /cards/:cardId/members/:id` (base URL `https://{{credentials.companyDomain}}.kaiten.ru/api/latest`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-member-role.md) for the provider-specific parameters and requirements.

