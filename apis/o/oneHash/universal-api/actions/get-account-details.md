# OneHash: Get Account Details

Retrieves account details from OneHash.

```
GET https://connect.mindcloud.co/v1/universal/oneHash/latest/actions/get-account-details
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OneHash `connectionId` ([setup](../authentication.md)).

## Example request

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

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `accountId` | string | no | OneHash Chat account id. |

## Response

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

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date |  |
| `features.agentManagement` | boolean |  |
| `features.auditLogs` | boolean |  |
| `features.automations` | boolean |  |
| `features.autoResolveConversations` | boolean |  |
| `features.campaigns` | boolean |  |
| `features.cannedResponses` | boolean |  |
| `features.channelEmail` | boolean |  |
| `features.channelFacebook` | boolean |  |
| `features.channelInstagram` | boolean |  |
| `features.channelTwitter` | boolean |  |
| `features.channelWebsite` | boolean |  |
| `features.chatwootV4` | boolean |  |
| `features.contactChatwootSupportTeam` | boolean |  |
| `features.crm` | boolean |  |
| `features.customAttributes` | boolean |  |
| `features.customReplyDomain` | boolean |  |
| `features.customReplyEmail` | boolean |  |
| `features.emailContinuityOnApiChannel` | boolean |  |
| `features.helpCenter` | boolean |  |
| `features.helpCenterEmbeddingSearch` | boolean |  |
| `features.inboundEmails` | boolean |  |
| `features.inboxManagement` | boolean |  |
| `features.integrations` | boolean |  |
| `features.ipLookup` | boolean |  |
| `features.labels` | boolean |  |
| `features.linearIntegration` | boolean |  |
| `features.macros` | boolean |  |
| `features.reports` | boolean |  |
| `features.reportV4` | boolean |  |
| `features.shopifyIntegration` | boolean |  |
| `features.sla` | boolean |  |
| `features.teamManagement` | boolean |  |
| `features.voiceRecorder` | boolean |  |
| `id` | number |  |
| `latestChatwootVersion` | string |  |
| `locale` | string |  |
| `name` | string |  |
| `status` | string |  |
| `supportEmail` | string |  |

## Native endpoint

Through the native OneHash API, this operation is `GET /api/v1/accounts/:accountId` (base URL `https://chat.onehash.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-account-details.md) for the provider-specific parameters and requirements.

