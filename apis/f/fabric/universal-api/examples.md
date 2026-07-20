# Fabric Universal API Examples

These examples use the MindCloud API key and Fabric connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Workspace



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

Example response:

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

See the full [Get Workspace action reference](actions/get-workspace.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/fabric/latest/actions/get-workspace).

## Confirm Workspace Deletion



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/fabric/latest/actions/confirm-workspace-deletion" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/fabric/latest/actions/confirm-workspace-deletion', {
  method: 'POST',
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

Example response:

```json
{
  "success": true,
  "data": [
    {
      "success": true
    }
  ],
  "meta": {}
}
```

See the full [Confirm Workspace Deletion action reference](actions/confirm-workspace-deletion.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/fabric/latest/actions/confirm-workspace-deletion).
