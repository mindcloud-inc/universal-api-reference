# Channels: List Users

Retrieves users from Channels.

```
GET https://connect.mindcloud.co/v1/universal/channels/latest/actions/list-users
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Channels `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/channels/latest/actions/list-users?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/channels/latest/actions/list-users?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "": [
        {
          "doNotAcceptIncomingCalls": true,
          "enabled": true,
          "id": 1,
          "missedIncomingCallsNotification": true,
          "msisdns": [
            "string"
          ],
          "name": "Ava Chen",
          "privatePhoneNumber": "string",
          "role": "string",
          "roleId": 1,
          "state": "string",
          "surname": "Ava Chen",
          "username": "Ava Chen"
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
| `[].doNotAcceptIncomingCalls` | boolean |  |
| `[].enabled` | boolean |  |
| `[].id` | number |  |
| `[].missedIncomingCallsNotification` | boolean |  |
| `[].msisdns[]` | string |  |
| `[].name` | string |  |
| `[].privatePhoneNumber` | string |  |
| `[].role` | string |  |
| `[].roleId` | number |  |
| `[].state` | string |  |
| `[].surname` | string |  |
| `[].username` | string |  |

## Native endpoint

Through the native Channels API, this operation is `GET /api/v1/users` (base URL `https://api.channels.app`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-users.md) for the provider-specific parameters and requirements.

