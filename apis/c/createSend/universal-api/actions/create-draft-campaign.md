# CreateSend: Create Draft Campaign

Creates a draft campaign in CreateSend.

```
POST https://connect.mindcloud.co/v1/universal/createSend/latest/actions/create-draft-campaign
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CreateSend `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/createSend/latest/actions/create-draft-campaign" \
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
const response = await fetch('https://connect.mindcloud.co/v1/universal/createSend/latest/actions/create-draft-campaign', {
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
| `clientId` | string | yes |  |
| `name` | string | yes |  |
| `subject` | string | yes |  |
| `fromName` | string | yes |  |
| `fromEmail` | string | yes |  |
| `replyTo` | string | yes |  |
| `htmlUrl` | string | yes |  |
| `textUrl` | string | no |  |
| `listIds[]` | array<string> | no |  |
| `segmentIds[]` | array<string> | no |  |
| `inlineCss` | boolean | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "campaignId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `campaignId` | string | Identifier of the created draft campaign. |

## Native endpoint

Through the native CreateSend API, this operation is `POST /campaigns/:clientId.json` (base URL `https://api.createsend.com/api/v3.3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-draft-campaign.md) for the provider-specific parameters and requirements.

