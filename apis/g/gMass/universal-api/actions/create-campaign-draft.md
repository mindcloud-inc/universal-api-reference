# GMass: Create Campaign Draft

Creates a Gmail draft for a GMass campaign.

```
POST https://connect.mindcloud.co/v1/universal/gMass/latest/actions/create-campaign-draft
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GMass `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/gMass/latest/actions/create-campaign-draft" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "subject": "string",
  "message": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/gMass/latest/actions/create-campaign-draft', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "subject": "string",
    "message": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `subject` | string | yes |  |
| `message` | string | yes |  |
| `fromEmail` | string | no |  |
| `messageType` | string | no |  |
| `listAddress` | string | no |  |
| `emailAddresses` | string | no |  |
| `cc` | string | no |  |
| `bcc` | string | no |  |
| `attachments[]` | array<object> | no |  |
| `attachments[].fileName` | string | no |  |
| `attachments[].base64Content` | string | no |  |
| `attachments[].contentType` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "attachments": [
        {
          "base64Content": "string",
          "contentType": "string",
          "fileName": "Ava Chen"
        }
      ],
      "bcc": "string",
      "campaignDraftId": "string",
      "cc": "string",
      "emailAddresses": "ava@example.com",
      "fromEmail": "ava@example.com",
      "listAddress": "string",
      "message": "string",
      "messageType": "string",
      "subject": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `attachments[].base64Content` | string |  |
| `attachments[].contentType` | string |  |
| `attachments[].fileName` | string |  |
| `bcc` | string |  |
| `campaignDraftId` | string |  |
| `cc` | string |  |
| `emailAddresses` | string |  |
| `fromEmail` | string |  |
| `listAddress` | string |  |
| `message` | string |  |
| `messageType` | string |  |
| `subject` | string |  |

## Native endpoint

Through the native GMass API, this operation is `POST /campaigndrafts` (base URL `https://api.gmass.co/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-campaign-draft.md) for the provider-specific parameters and requirements.

