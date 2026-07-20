# OneSignal: Create User

Creates a user in OneSignal.

```
POST https://connect.mindcloud.co/v1/universal/oneSignal/latest/actions/create-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OneSignal `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/oneSignal/latest/actions/create-user" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "identity": {},
  "subscriptions[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/oneSignal/latest/actions/create-user', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "identity": {},
    "subscriptions[]": [{}]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `identity` | object | yes | An object of user aliases, such as {"external_id":"user-123"}. |
| `subscriptions[]` | array<object> | yes | An array of subscription objects to attach to the user. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "identity": {
        "externalId": "string",
        "onesignalId": "string"
      },
      "subscriptions": [
        {
          "appId": "string",
          "id": "string",
          "token": "string",
          "type": "string"
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `identity.externalId` | string |  |
| `identity.onesignalId` | string |  |
| `subscriptions[].appId` | string |  |
| `subscriptions[].id` | string |  |
| `subscriptions[].token` | string |  |
| `subscriptions[].type` | string |  |

## Native endpoint

Through the native OneSignal API, this operation is `POST /apps/:app_id/users` (base URL `https://api.onesignal.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-user.md) for the provider-specific parameters and requirements.

