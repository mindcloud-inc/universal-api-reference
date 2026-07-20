# Kaiten: Add Member to Card

Adds a member to a Kaiten card.

```
POST https://connect.mindcloud.co/v1/universal/kaiten/latest/actions/add-member-to-card
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Kaiten `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/kaiten/latest/actions/add-member-to-card" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "cardId": 1,
  "userId": 1,
  "type": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/kaiten/latest/actions/add-member-to-card', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "cardId": 1,
    "userId": 1,
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
| `userId` | number | yes | The Kaiten user ID to add to the card. |
| `type` | number | yes | The numeric member role type. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "avatar_initials_url": "https://example.com",
      "avatar_type": 1,
      "avatar_uploaded_url": "https://example.com",
      "email": "ava@example.com",
      "full_name": "Ava Chen",
      "id": 1,
      "initials": "string",
      "lng": "string",
      "theme": "string",
      "timezone": "string",
      "type": 1,
      "updated": "string",
      "username": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `avatar_initials_url` | string |  |
| `avatar_type` | number |  |
| `avatar_uploaded_url` | string |  |
| `email` | string |  |
| `full_name` | string |  |
| `id` | number |  |
| `initials` | string |  |
| `lng` | string |  |
| `theme` | string |  |
| `timezone` | string |  |
| `type` | number |  |
| `updated` | string |  |
| `username` | string |  |

## Native endpoint

Through the native Kaiten API, this operation is `POST /cards/:cardId/members` (base URL `https://{{credentials.companyDomain}}.kaiten.ru/api/latest`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-member-to-card.md) for the provider-specific parameters and requirements.

