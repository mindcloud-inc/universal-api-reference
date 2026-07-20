# Cliengo: Create Conversation



```
POST https://connect.mindcloud.co/v1/universal/cliengo/latest/actions/create-conversation
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cliengo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/cliengo/latest/actions/create-conversation" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "companyId": "string",
  "websiteId": "string",
  "channel": "WEB",
  "from": "apps+cliengo-conversation@example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/cliengo/latest/actions/create-conversation', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "companyId": "string",
    "websiteId": "string",
    "channel": "WEB",
    "from": "apps+cliengo-conversation@example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `companyId` | string | yes | The Cliengo company ID that owns the conversation. |
| `websiteId` | string | yes | The Cliengo website ID where the conversation should be created. |
| `channel` | string | yes | The conversation channel. Verified working value: WEB. Example: `WEB`. |
| `from` | string | yes | The visitor identifier for the conversation, such as an email address. Example: `apps+cliengo-conversation@example.com`. |
| `url` | string | no | Optional source URL associated with the conversation. Example: `https://mindcloud.co`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "assignedTo": "string",
      "channel": "string",
      "clientName": "Ava Chen",
      "companyId": "string",
      "conversationContext": {},
      "creationDate": "2026-05-07T12:00:00.000Z",
      "from": "string",
      "id": "string",
      "intercepted": true,
      "isClosed": true,
      "operatorTags": [
        "string"
      ],
      "participants": [
        {}
      ],
      "persistentLastOperator": "string",
      "phaseHistory": [
        {}
      ],
      "phaseId": "string",
      "status": "string",
      "supportTicket": [
        {}
      ],
      "tags": [
        "string"
      ],
      "type": "string",
      "url": "https://example.com",
      "visitorColor": "string",
      "websiteId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `assignedTo` | string |  |
| `channel` | string |  |
| `clientName` | string |  |
| `companyId` | string |  |
| `conversationContext` | object |  |
| `creationDate` | date |  |
| `from` | string |  |
| `id` | string |  |
| `intercepted` | boolean |  |
| `isClosed` | boolean |  |
| `operatorTags` | array<string> |  |
| `participants` | array<object> |  |
| `persistentLastOperator` | string |  |
| `phaseHistory` | array<object> |  |
| `phaseId` | string |  |
| `status` | string |  |
| `supportTicket` | array<object> |  |
| `tags` | array<string> |  |
| `type` | string |  |
| `url` | string |  |
| `visitorColor` | string |  |
| `websiteId` | string |  |

## Native endpoint

Through the native Cliengo API, this operation is `POST /conversations` (base URL `https://api.cliengo.com/1.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-conversation.md) for the provider-specific parameters and requirements.

