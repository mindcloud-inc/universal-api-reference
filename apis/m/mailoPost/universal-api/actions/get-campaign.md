# MailoPost: Get Campaign

Retrieves a campaign from MailoPost.

```
GET https://connect.mindcloud.co/v1/universal/mailoPost/latest/actions/get-campaign
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MailoPost `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mailoPost/latest/actions/get-campaign?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mailoPost/latest/actions/get-campaign?${params}`, {
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

Through the native MailoPost API, this operation is `GET /email/campaigns/:id` (base URL `https://api.mailopost.ru/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-campaign.md) for the provider-specific parameters and requirements.

