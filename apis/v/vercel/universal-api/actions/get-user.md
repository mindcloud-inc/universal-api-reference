# Vercel: Get User

Retrieves the authenticated user from Vercel.

```
GET https://connect.mindcloud.co/v1/universal/vercel/latest/actions/get-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Vercel `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/vercel/latest/actions/get-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/vercel/latest/actions/get-user?${params}`, {
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
      "avatar": {},
      "billing": {
        "address": {},
        "cancelation": {},
        "currency": "string",
        "email": {},
        "language": {},
        "name": {},
        "period": {},
        "plan": "string",
        "platform": "string",
        "status": "string",
        "tax": {},
        "trial": {}
      },
      "createdAt": 1,
      "dataCache": {
        "excessBillingEnabled": true
      },
      "defaultTeamId": "string",
      "email": "ava@example.com",
      "hasTrialAvailable": true,
      "id": "string",
      "name": {},
      "remoteCaching": {
        "enabled": true
      },
      "resourceConfig": {
        "concurrentBuilds": 1
      },
      "softBlock": {},
      "stagingPrefix": "string",
      "username": "Ava Chen",
      "version": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `avatar` | object |  |
| `billing.address` | object |  |
| `billing.cancelation` | object |  |
| `billing.currency` | string |  |
| `billing.email` | object |  |
| `billing.language` | object |  |
| `billing.name` | object |  |
| `billing.period` | object |  |
| `billing.plan` | string |  |
| `billing.platform` | string |  |
| `billing.status` | string |  |
| `billing.tax` | object |  |
| `billing.trial` | object |  |
| `createdAt` | number |  |
| `dataCache.excessBillingEnabled` | boolean |  |
| `defaultTeamId` | string |  |
| `email` | string |  |
| `hasTrialAvailable` | boolean |  |
| `id` | string |  |
| `name` | object |  |
| `remoteCaching.enabled` | boolean |  |
| `resourceConfig.concurrentBuilds` | number |  |
| `softBlock` | object |  |
| `stagingPrefix` | string |  |
| `username` | string |  |
| `version` | string |  |

## Native endpoint

Through the native Vercel API, this operation is `GET /v2/user` (base URL `https://api.vercel.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-user.md) for the provider-specific parameters and requirements.

