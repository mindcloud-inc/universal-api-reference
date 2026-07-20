# LoginRadius: Change Phone Number

Updates a phone number in LoginRadius.

```
PUT https://connect.mindcloud.co/v1/universal/loginRadius/latest/actions/change-phone-number
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LoginRadius `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/loginRadius/latest/actions/change-phone-number" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "accessToken": "seeded-access-token",
  "phone": "+15551234567"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/loginRadius/latest/actions/change-phone-number', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "accessToken": "seeded-access-token",
    "phone": "+15551234567"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `accessToken` | string | yes | Access Token of the user. Example: `seeded-access-token`. |
| `phone` | string | yes | New phone number. Example: `+15551234567`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native LoginRadius API returns.

## Native endpoint

Through the native LoginRadius API, this operation is `PUT /identity/v2/auth/phone` (base URL `https://api.loginradius.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/change-phone-number.md) for the provider-specific parameters and requirements.

