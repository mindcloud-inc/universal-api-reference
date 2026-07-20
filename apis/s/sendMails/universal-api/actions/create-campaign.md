# SendMails: Create Campaign

Creates a new campaign in SendMails.

```
POST https://connect.mindcloud.co/v1/universal/sendMails/latest/actions/create-campaign
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SendMails `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/sendMails/latest/actions/create-campaign" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "listUid": "string",
  "name": "Ava Chen",
  "subject": "string",
  "fromEmail": "ava@example.com",
  "fromName": "Ava Chen",
  "replyTo": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/sendMails/latest/actions/create-campaign', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "listUid": "string",
    "name": "Ava Chen",
    "subject": "string",
    "fromEmail": "ava@example.com",
    "fromName": "Ava Chen",
    "replyTo": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `listUid` | string | yes | List UID. |
| `name` | string | yes | Campaign name. |
| `subject` | string | yes | Email subject. |
| `fromEmail` | string | yes | From email address. |
| `fromName` | string | yes | From name. |
| `replyTo` | string | yes | Reply-to email address. |
| `trackOpen` | string | no | Track email opens. |
| `trackClick` | string | no | Track email clicks. |
| `signDkim` | string | no | Sign with DKIM. |
| `skipFailedMessages` | string | no | Skip failed messages. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "attributes": {},
      "message": "string",
      "status": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `attributes` | object | Created campaign attributes. |
| `message` | string | Provider result message. |
| `status` | number | Provider success indicator. |

## Native endpoint

Through the native SendMails API, this operation is `POST /campaigns` (base URL `https://app.sendmails.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-campaign.md) for the provider-specific parameters and requirements.

