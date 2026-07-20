# Late: Get Usage Stats



```
GET https://connect.mindcloud.co/v1/universal/late/latest/actions/get-usage-stats
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Late `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/late/latest/actions/get-usage-stats?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/late/latest/actions/get-usage-stats?${params}`, {
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
      "autoUpgradeEnabled": true,
      "billingAnchorDay": 1,
      "billingPeriod": "string",
      "hasAccess": true,
      "isAppSumo": true,
      "isInvitedUser": true,
      "isRestrictedUser": true,
      "limits": {},
      "planName": "Ava Chen",
      "signupDate": "2026-05-07T12:00:00.000Z",
      "suspendedAt": "2026-05-07T12:00:00.000Z",
      "usage": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `autoUpgradeEnabled` | boolean | Whether automatic upgrades are enabled. |
| `billingAnchorDay` | number | Billing reset day of month. |
| `billingPeriod` | string | Billing cadence. |
| `hasAccess` | boolean | Whether the workspace can currently use the product. |
| `isAppSumo` | boolean | Whether the plan is AppSumo-based. |
| `isInvitedUser` | boolean | Whether the credential belongs to an invited user. |
| `isRestrictedUser` | boolean | Whether the user is restricted. |
| `limits` | object | Plan usage limits. |
| `planName` | string | Current plan name. |
| `signupDate` | date | Workspace signup timestamp. |
| `suspendedAt` | date | Suspension timestamp when present. |
| `usage` | object | Current usage counters. |

## Native endpoint

Through the native Late API, this operation is `GET /usage-stats` (base URL `https://zernio.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-usage-stats.md) for the provider-specific parameters and requirements.

