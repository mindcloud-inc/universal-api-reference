# BotStar: Update User Attributes



```
PUT https://connect.mindcloud.co/v1/universal/botStar/latest/actions/update-user-attributes
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BotStar `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/botStar/latest/actions/update-user-attributes" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "botId": "string",
  "userId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/botStar/latest/actions/update-user-attributes', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "botId": "string",
    "userId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `birthday` | string | no |  |
| `botId` | string | yes |  |
| `email` | string | no |  |
| `firstName` | string | no |  |
| `gender` | string | no |  |
| `lastName` | string | no |  |
| `userId` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "birthday": "2026-05-07T12:00:00.000Z",
      "email": "ava@example.com",
      "first_name": "Ava",
      "gender": "string",
      "last_name": "Chen",
      "some_custom_attributes1": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `birthday` | date |  |
| `email` | string |  |
| `first_name` | string |  |
| `gender` | string |  |
| `last_name` | string |  |
| `some_custom_attributes1` | string |  |

## Native endpoint

Through the native BotStar API, this operation is `PATCH /bots/:botId/users/:userId` (base URL `https://apis.botstar.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-user-attributes.md) for the provider-specific parameters and requirements.

