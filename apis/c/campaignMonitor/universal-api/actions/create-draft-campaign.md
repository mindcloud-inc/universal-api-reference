# Campaign Monitor: Create Draft Campaign

Creates a draft campaign in Campaign Monitor.

```
POST https://connect.mindcloud.co/v1/universal/campaignMonitor/latest/actions/create-draft-campaign
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Campaign Monitor `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/campaignMonitor/latest/actions/create-draft-campaign" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "clientId": "string",
  "name": "Ava Chen",
  "subject": "string",
  "fromName": "Ava Chen",
  "fromEmail": "ava@example.com",
  "replyTo": "string",
  "htmlUrl": "https://example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/campaignMonitor/latest/actions/create-draft-campaign', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "clientId": "string",
    "name": "Ava Chen",
    "subject": "string",
    "fromName": "Ava Chen",
    "fromEmail": "ava@example.com",
    "replyTo": "string",
    "htmlUrl": "https://example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `clientId` | string | yes | Campaign Monitor client identifier. |
| `name` | string | yes | Internal name of the campaign. |
| `subject` | string | yes | Campaign email subject line. |
| `fromName` | string | yes | Sender name for the campaign. |
| `fromEmail` | string | yes | Sender email address for the campaign. |
| `replyTo` | string | yes | Reply-to email address for the campaign. |
| `htmlUrl` | string | yes | URL of the hosted HTML content for the campaign. |
| `textUrl` | string | no | URL of the hosted plain-text content for the campaign. |
| `listIds[]` | array<string> | no | Recipient list identifiers for the campaign. |
| `segmentIds[]` | array<string> | no | Recipient segment identifiers for the campaign. |
| `inlineCss` | boolean | no | Whether to inline CSS when creating the campaign. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "response": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `response` | string |  |

## Native endpoint

Through the native Campaign Monitor API, this operation is `POST /campaigns/:clientId.json` (base URL `https://api.createsend.com/api/v3.3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-draft-campaign.md) for the provider-specific parameters and requirements.

