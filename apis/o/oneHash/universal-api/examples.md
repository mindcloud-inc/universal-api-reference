# OneHash Universal API Examples

These examples use the MindCloud API key and OneHash connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Account Details

Retrieves account details from OneHash.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/oneHash/latest/actions/get-account-details?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/oneHash/latest/actions/get-account-details?${params}`, {
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
      "createdAt": "2026-05-07T12:00:00.000Z",
      "features": {
        "agentManagement": true,
        "auditLogs": true,
        "automations": true,
        "autoResolveConversations": true,
        "campaigns": true,
        "cannedResponses": true,
        "channelEmail": true,
        "channelFacebook": true,
        "channelInstagram": true,
        "channelTwitter": true,
        "channelWebsite": true,
        "chatwootV4": true,
        "contactChatwootSupportTeam": true,
        "crm": true,
        "customAttributes": true,
        "customReplyDomain": true,
        "customReplyEmail": true,
        "emailContinuityOnApiChannel": true,
        "helpCenter": true,
        "helpCenterEmbeddingSearch": true,
        "inboundEmails": true,
        "inboxManagement": true,
        "integrations": true,
        "ipLookup": true,
        "labels": true,
        "linearIntegration": true,
        "macros": true,
        "reports": true,
        "reportV4": true,
        "shopifyIntegration": true,
        "sla": true,
        "teamManagement": true,
        "voiceRecorder": true
      },
      "id": 1,
      "latestChatwootVersion": "string",
      "locale": "string",
      "name": "Ava Chen",
      "status": "string",
      "supportEmail": "ava@example.com"
    }
  ],
  "meta": {}
}
```

See the full [Get Account Details action reference](actions/get-account-details.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/oneHash/latest/actions/get-account-details).

## Add Contact Labels

Updates a contact's labels in OneHash.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/oneHash/latest/actions/add-contact-labels" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/oneHash/latest/actions/add-contact-labels', {
  method: 'PUT',
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
  "data": [],
  "meta": {}
}
```

See the full [Add Contact Labels action reference](actions/add-contact-labels.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/oneHash/latest/actions/add-contact-labels).
