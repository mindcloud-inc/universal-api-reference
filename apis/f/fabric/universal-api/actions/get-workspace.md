# Fabric: Get Workspace



```
GET https://connect.mindcloud.co/v1/universal/fabric/latest/actions/get-workspace
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Fabric `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fabric/latest/actions/get-workspace?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fabric/latest/actions/get-workspace?${params}`, {
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
      "avatarStoragePath": "string",
      "avatarUrl": "https://example.com",
      "createdAt": "string",
      "deletedAt": "string",
      "description": "string",
      "id": "string",
      "isFreeTrialAvailable": true,
      "marketing": {},
      "membersCount": 1,
      "modifiedAt": "string",
      "parentWorkspaceId": "string",
      "planBilling": "string",
      "planHasDefaultPaymentMethod": true,
      "planModifiedAt": "string",
      "planStatus": "string",
      "planStoreId": "string",
      "planStoreType": "string",
      "planTier": "string",
      "referral": {},
      "referralCode": "string",
      "rewardfulReferral": "string",
      "slug": "string",
      "stripeCustomerId": "string",
      "title": "string",
      "trialEndingAt": "string",
      "type": "string",
      "userId": "string",
      "workspaceRoles": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `avatarStoragePath` | string |  |
| `avatarUrl` | string |  |
| `createdAt` | string |  |
| `deletedAt` | string |  |
| `description` | string |  |
| `id` | string |  |
| `isFreeTrialAvailable` | boolean |  |
| `marketing` | object |  |
| `membersCount` | number |  |
| `modifiedAt` | string |  |
| `parentWorkspaceId` | string |  |
| `planBilling` | string |  |
| `planHasDefaultPaymentMethod` | boolean |  |
| `planModifiedAt` | string |  |
| `planStatus` | string |  |
| `planStoreId` | string |  |
| `planStoreType` | string |  |
| `planTier` | string |  |
| `referral` | object |  |
| `referralCode` | string |  |
| `rewardfulReferral` | string |  |
| `slug` | string |  |
| `stripeCustomerId` | string |  |
| `title` | string |  |
| `trialEndingAt` | string |  |
| `type` | string |  |
| `userId` | string |  |
| `workspaceRoles` | array<object> |  |

## Native endpoint

Through the native Fabric API, this operation is `GET /v2/workspaces/me` (base URL `https://api.fabric.so`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-workspace.md) for the provider-specific parameters and requirements.

