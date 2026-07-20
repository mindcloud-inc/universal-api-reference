# Week Plan: Add User Email



```
PUT https://connect.mindcloud.co/v1/universal/weekPlan/latest/actions/add-user-email
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Week Plan `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/weekPlan/latest/actions/add-user-email" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/weekPlan/latest/actions/add-user-email', {
  method: 'PUT',
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
      "Email": "ava@example.com",
      "EmailVerified": true,
      "Message": "string",
      "UserId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `Email` | string |  |
| `EmailVerified` | boolean |  |
| `Message` | string |  |
| `UserId` | number |  |

## Native endpoint

Through the native Week Plan API, this operation is `POST users/add_email` (base URL `https://api.weekplan.net/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-user-email.md) for the provider-specific parameters and requirements.

