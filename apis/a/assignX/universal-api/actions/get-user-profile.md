# AssignX: Get User Profile

Retrieves the current user profile from AssignX.

```
GET https://connect.mindcloud.co/v1/universal/assignX/latest/actions/get-user-profile
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a AssignX `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/assignX/latest/actions/get-user-profile?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/assignX/latest/actions/get-user-profile?${params}`, {
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
      "categoryProfile": {
        "accountType": "string",
        "companySize": "string",
        "discoverySource": "string",
        "industry": "string"
      },
      "createdAt": "2026-05-07T12:00:00.000Z",
      "customClient": {},
      "customer": {},
      "defaultWorkspace": {},
      "deleted": true,
      "email": "ava@example.com",
      "Id": "string",
      "locationData": "string",
      "name": "Ava Chen",
      "news": {
        "usual": "string"
      },
      "provider": "string",
      "providerId": "string",
      "roles": "string",
      "status": 1,
      "subscription": {
        "active": true,
        "agents": {
          "currentUsage": 1,
          "limit": 1
        },
        "axTokensPackage": {
          "currentUsage": 1,
          "limit": 1
        },
        "axTokensPlan": {
          "currentUsage": 1,
          "limit": 1
        },
        "billingFrequency": "string",
        "status": 1,
        "storage": {
          "currentUsage": 1,
          "limit": 1
        },
        "tier": 1,
        "validity": "2026-05-07T12:00:00.000Z"
      },
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "V": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `avatar` | object |  |
| `categoryProfile.accountType` | string |  |
| `categoryProfile.companySize` | string |  |
| `categoryProfile.discoverySource` | string |  |
| `categoryProfile.industry` | string |  |
| `createdAt` | date |  |
| `customClient` | object |  |
| `customer` | object |  |
| `defaultWorkspace` | object |  |
| `deleted` | boolean |  |
| `email` | string |  |
| `Id` | string |  |
| `locationData` | string |  |
| `name` | string |  |
| `news.usual` | string |  |
| `provider` | string |  |
| `providerId` | string |  |
| `roles` | string |  |
| `status` | number |  |
| `subscription.active` | boolean |  |
| `subscription.agents.currentUsage` | number |  |
| `subscription.agents.limit` | number |  |
| `subscription.axTokensPackage.currentUsage` | number |  |
| `subscription.axTokensPackage.limit` | number |  |
| `subscription.axTokensPlan.currentUsage` | number |  |
| `subscription.axTokensPlan.limit` | number |  |
| `subscription.billingFrequency` | string |  |
| `subscription.status` | number |  |
| `subscription.storage.currentUsage` | number |  |
| `subscription.storage.limit` | number |  |
| `subscription.tier` | number |  |
| `subscription.validity` | date |  |
| `updatedAt` | date |  |
| `V` | number |  |

## Native endpoint

Through the native AssignX API, this operation is `GET getProfile` (base URL `https://api.agentx.so/api/v1/access/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-user-profile.md) for the provider-specific parameters and requirements.

