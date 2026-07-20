# MailoPost: Create Campaign

Creates a new campaign in MailoPost.

```
POST https://connect.mindcloud.co/v1/universal/mailoPost/latest/actions/create-campaign
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MailoPost `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/mailoPost/latest/actions/create-campaign" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "fromEmail": "ava@example.com",
  "subject": "string",
  "html": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/mailoPost/latest/actions/create-campaign', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "fromEmail": "ava@example.com",
    "subject": "string",
    "html": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `fromEmail` | string | yes | Sender email address. |
| `subject` | string | yes | Campaign subject line. |
| `text` | string | no | Plain-text campaign body. |
| `html` | string | yes | HTML campaign body. |
| `segmentId` | string | no | Segment ID to send the campaign to. |
| `lists[]` | array<object> | no | Recipient lists to send the campaign to. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `fromName` | string | no | Sender display name. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "from_email": "ava@example.com",
      "from_name": "Ava Chen",
      "html": "string",
      "id": 1,
      "purchase": {
        "credits": 1,
        "deficit": 1,
        "enable": true,
        "subscribers": 1
      },
      "recipients_count": 1,
      "state": "string",
      "statistics": {
        "bounced": 1,
        "delivered": 1
      },
      "text": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `from_email` | string |  |
| `from_name` | string |  |
| `html` | string |  |
| `id` | number |  |
| `purchase.credits` | number |  |
| `purchase.deficit` | number |  |
| `purchase.enable` | boolean |  |
| `purchase.subscribers` | number |  |
| `recipients_count` | number |  |
| `state` | string |  |
| `statistics.bounced` | number |  |
| `statistics.delivered` | number |  |
| `text` | string |  |

## Native endpoint

Through the native MailoPost API, this operation is `POST /email/campaigns` (base URL `https://api.mailopost.ru/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-campaign.md) for the provider-specific parameters and requirements.

