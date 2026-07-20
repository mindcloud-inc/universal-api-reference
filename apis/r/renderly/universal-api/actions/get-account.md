# Renderly: Get Account

Retrieves account details and credits from Renderly.

```
GET https://connect.mindcloud.co/v1/universal/renderly/latest/actions/get-account
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Renderly `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/renderly/latest/actions/get-account?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/renderly/latest/actions/get-account?${params}`, {
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
      "apiKey": {
        "createdAt": "2026-05-07T12:00:00.000Z",
        "lastUsed": "2026-05-07T12:00:00.000Z",
        "prefix": "string"
      },
      "recentTransactions": [
        {
          "amountInCents": 1,
          "createdAt": "2026-05-07T12:00:00.000Z",
          "credits": 1,
          "currency": "string",
          "id": "string",
          "status": "string",
          "type": "string"
        }
      ],
      "usage": {
        "completedJobs": 1,
        "failedJobs": 1,
        "pendingJobs": 1,
        "totalCreditsUsed": 1,
        "totalRenderJobs": 1
      },
      "user": {
        "createdAt": "2026-05-07T12:00:00.000Z",
        "credits": 1,
        "email": "ava@example.com",
        "id": "string",
        "name": "Ava Chen",
        "role": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `apiKey` | object |  |
| `apiKey.createdAt` | date |  |
| `apiKey.lastUsed` | date |  |
| `apiKey.prefix` | string |  |
| `recentTransactions` | array<object> |  |
| `recentTransactions[].amountInCents` | number |  |
| `recentTransactions[].createdAt` | date |  |
| `recentTransactions[].credits` | number |  |
| `recentTransactions[].currency` | string |  |
| `recentTransactions[].id` | string |  |
| `recentTransactions[].status` | string |  |
| `recentTransactions[].type` | string |  |
| `usage` | object |  |
| `usage.completedJobs` | number |  |
| `usage.failedJobs` | number |  |
| `usage.pendingJobs` | number |  |
| `usage.totalCreditsUsed` | number |  |
| `usage.totalRenderJobs` | number |  |
| `user` | object |  |
| `user.createdAt` | date |  |
| `user.credits` | number |  |
| `user.email` | string |  |
| `user.id` | string |  |
| `user.name` | string |  |
| `user.role` | string |  |

## Native endpoint

Through the native Renderly API, this operation is `GET /account` (base URL `https://renderly.video/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-account.md) for the provider-specific parameters and requirements.

