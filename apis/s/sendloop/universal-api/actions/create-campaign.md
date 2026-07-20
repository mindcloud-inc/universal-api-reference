# Sendloop: Create Campaign



```
POST https://connect.mindcloud.co/v1/universal/sendloop/latest/actions/create-campaign
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sendloop `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/sendloop/latest/actions/create-campaign" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen",
  "fromName": "Ava Chen",
  "fromEmail": "ava@example.com",
  "replyToName": "Ava Chen",
  "replyToEmail": "ava@example.com",
  "recipients": "string",
  "subject": "string",
  "htmlContent": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/sendloop/latest/actions/create-campaign', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen",
    "fromName": "Ava Chen",
    "fromEmail": "ava@example.com",
    "replyToName": "Ava Chen",
    "replyToEmail": "ava@example.com",
    "recipients": "string",
    "subject": "string",
    "htmlContent": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | Name of your campaign |
| `fromName` | string | yes | The name shown in the from email header |
| `fromEmail` | string | yes | Sender email address |
| `replyToName` | string | yes | The name shown in the reply-to header |
| `replyToEmail` | string | yes | Email address to receive replies |
| `recipients` | string | yes | ID numbers of recipient lists |
| `subject` | string | yes | Subject of your email campaign |
| `plainContent` | string | no | Text content of your email campaign |
| `htmlContent` | string | yes | HTML content of your email campaign |

## Response

```json
{
  "success": true,
  "data": [
    {
      "availableRecipients": 1,
      "campaignID": "string",
      "estimatedRecipients": 1,
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `availableRecipients` | number |  |
| `campaignID` | string |  |
| `estimatedRecipients` | number |  |
| `success` | boolean |  |

## Native endpoint

Through the native Sendloop API, this operation is `POST /campaign.create/json` (base URL `https://{{credentials.subdomain}}.sendloop.com/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-campaign.md) for the provider-specific parameters and requirements.

