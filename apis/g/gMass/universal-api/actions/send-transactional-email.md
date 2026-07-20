# GMass: Send Transactional Email

Sends a transactional email through GMass.

```
POST https://connect.mindcloud.co/v1/universal/gMass/latest/actions/send-transactional-email
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GMass `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/gMass/latest/actions/send-transactional-email" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "to": "string",
  "subject": "string",
  "message": "string",
  "fromEmail": "ava@example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/gMass/latest/actions/send-transactional-email', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "to": "string",
    "subject": "string",
    "message": "string",
    "fromEmail": "ava@example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `to` | string | yes |  |
| `subject` | string | yes |  |
| `message` | string | yes |  |
| `fromEmail` | string | yes |  |
| `fromName` | string | no |  |
| `cc` | string | no |  |
| `bcc` | string | no |  |
| `messageRaw` | string | no |  |
| `settings` | object | no |  |
| `settings.openTrack` | boolean | no |  |
| `settings.clickTrack` | boolean | no |  |
| `settings.messageType` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "bcc": "string",
      "cc": "string",
      "fromEmail": "ava@example.com",
      "fromName": "Ava Chen",
      "message": "string",
      "messageRaw": "string",
      "settings": {
        "clickTrack": true,
        "listUnsubscribeHeader": true,
        "messageType": "string",
        "openTrack": true,
        "smtpRelay": true,
        "SmtpServerId": 1,
        "threadToCampaign": 1,
        "useCustomerSmtp": true
      },
      "subject": "string",
      "to": "string",
      "transactionalEmailId": "ava@example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `bcc` | string |  |
| `cc` | string |  |
| `fromEmail` | string |  |
| `fromName` | string |  |
| `message` | string |  |
| `messageRaw` | string |  |
| `settings.clickTrack` | boolean |  |
| `settings.listUnsubscribeHeader` | boolean |  |
| `settings.messageType` | string |  |
| `settings.openTrack` | boolean |  |
| `settings.smtpRelay` | boolean |  |
| `settings.SmtpServerId` | number |  |
| `settings.threadToCampaign` | number |  |
| `settings.useCustomerSmtp` | boolean |  |
| `subject` | string |  |
| `to` | string |  |
| `transactionalEmailId` | string |  |

## Native endpoint

Through the native GMass API, this operation is `POST /transactional` (base URL `https://api.gmass.co/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-transactional-email.md) for the provider-specific parameters and requirements.

