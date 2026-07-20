# 2Smart Cloud: Reset mobile password



```
POST https://connect.mindcloud.co/v1/universal/smartCloud/latest/actions/create-users-reset-password
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a 2Smart Cloud `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/smartCloud/latest/actions/create-users-reset-password" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/smartCloud/latest/actions/create-users-reset-password', {
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
| `data` | object | no |  |
| `required` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created": "2026-05-07T12:00:00.000Z",
      "email": "ava@example.com",
      "fbPushTopic": "string",
      "id": 1,
      "isPasswordSet": true,
      "phoneNumber": "string",
      "updated": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created` | date |  |
| `email` | string |  |
| `fbPushTopic` | string |  |
| `id` | number |  |
| `isPasswordSet` | boolean |  |
| `phoneNumber` | string |  |
| `updated` | date |  |

## Native endpoint

Through the native 2Smart Cloud API, this operation is `POST /users/reset-password` (base URL `https://cloud.2smart.com/robot/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-users-reset-password.md) for the provider-specific parameters and requirements.

