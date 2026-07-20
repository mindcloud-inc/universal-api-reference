# MailoPost: Deliver Campaign

Delivers a MailoPost campaign immediately.

```
PUT https://connect.mindcloud.co/v1/universal/mailoPost/latest/actions/deliver-campaign
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MailoPost `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/mailoPost/latest/actions/deliver-campaign" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/mailoPost/latest/actions/deliver-campaign', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | MailoPost campaign identifier. |

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
      "start_at": "string",
      "state": "string",
      "text": "string",
      "time_zone": "string"
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
| `start_at` | string |  |
| `state` | string |  |
| `text` | string |  |
| `time_zone` | string |  |

## Native endpoint

Through the native MailoPost API, this operation is `PATCH /email/campaigns/:id/deliver` (base URL `https://api.mailopost.ru/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/deliver-campaign.md) for the provider-specific parameters and requirements.

