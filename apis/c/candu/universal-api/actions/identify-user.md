# Candu: Identify User

Updates a user profile in Candu.

```
PUT https://connect.mindcloud.co/v1/universal/candu/latest/actions/identify-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Candu `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/candu/latest/actions/identify-user" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "userId": "string",
  "traits": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/candu/latest/actions/identify-user', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "userId": "string",
    "traits": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `userId` | string | yes | The user ID to identify. |
| `traits` | object | yes | User traits to store in Candu. |
| `timestamp` | date | no | Optional event timestamp. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `success` | boolean | True when Candu accepts the event webhook request. |

## Native endpoint

Through the native Candu API, this operation is `POST /eventWebhook` (base URL `https://api.candu.ai/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/identify-user.md) for the provider-specific parameters and requirements.

