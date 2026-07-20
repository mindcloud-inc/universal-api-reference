# AssignX Universal API Examples

These examples use the MindCloud API key and AssignX connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get User Profile

Retrieves the current user profile from AssignX.

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

Example response:

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

See the full [Get User Profile action reference](actions/get-user-profile.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/assignX/latest/actions/get-user-profile).

## Create Conversation

Creates a new conversation in AssignX.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/assignX/latest/actions/create-conversation" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/assignX/latest/actions/create-conversation', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string"
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
      "bots": [
        "string"
      ],
      "contextUsage": {
        "contextWindowSize": 1,
        "lastUpdated": "2026-05-07T12:00:00.000Z",
        "messageCount": 1,
        "totalInputTokens": 1,
        "totalOutputTokens": 1,
        "totalTokens": 1,
        "usagePercentage": 1
      },
      "createdAt": "2026-05-07T12:00:00.000Z",
      "hasEnded": true,
      "Id": "string",
      "isPreview": true,
      "isSharedChat": true,
      "lastActivity": "2026-05-07T12:00:00.000Z",
      "name": {},
      "origin": "string",
      "title": {},
      "type": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "users": [
        "string"
      ],
      "V": 1,
      "vote": {}
    }
  ],
  "meta": {}
}
```

See the full [Create Conversation action reference](actions/create-conversation.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/assignX/latest/actions/create-conversation).
