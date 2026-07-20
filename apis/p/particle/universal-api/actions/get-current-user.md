# Particle: Get Current User



```
GET https://connect.mindcloud.co/v1/universal/particle/latest/actions/get-current-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Particle `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/particle/latest/actions/get-current-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/particle/latest/actions/get-current-user?${params}`, {
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
      "accountInfo": {
        "accountType": "string",
        "businessAccount": true,
        "businessCategory": "string",
        "companyName": "Ava Chen",
        "firstName": "Ava",
        "lastName": "Chen"
      },
      "cellularDeviceCount": 1,
      "memberships": [
        {}
      ],
      "mfa": {
        "enabled": true
      },
      "tos": {
        "accepted": true,
        "date": "string",
        "version": 1
      },
      "username": "Ava Chen",
      "wifiDeviceCount": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accountInfo.accountType` | string |  |
| `accountInfo.businessAccount` | boolean |  |
| `accountInfo.businessCategory` | string |  |
| `accountInfo.companyName` | string |  |
| `accountInfo.firstName` | string |  |
| `accountInfo.lastName` | string |  |
| `cellularDeviceCount` | number |  |
| `memberships` | array<object> |  |
| `mfa.enabled` | boolean |  |
| `tos.accepted` | boolean |  |
| `tos.date` | string |  |
| `tos.version` | number |  |
| `username` | string |  |
| `wifiDeviceCount` | number |  |

## Native endpoint

Through the native Particle API, this operation is `GET /v1/user` (base URL `https://api.particle.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-current-user.md) for the provider-specific parameters and requirements.

