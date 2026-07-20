# SendPulse: List Campaigns

Retrieves a list of campaigns from SendPulse.

```
GET https://connect.mindcloud.co/v1/universal/sendPulse/latest/actions/list-campaigns
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SendPulse `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sendPulse/latest/actions/list-campaigns?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sendPulse/latest/actions/list-campaigns?${params}`, {
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
| `limit` | number | no | Maximum number of campaigns to return. Example: `100`. |
| `offset` | number | no | Number of campaigns to skip before returning results. Example: `0`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `status` | string | no | Filter campaigns by status. Example: `draft`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "all_email_qty": 1,
      "company_price": "string",
      "id": 1,
      "is_sms": true,
      "is_viber": true,
      "message": {
        "attachments": "string",
        "list_id": 1,
        "sender_email": "ava@example.com",
        "sender_name": "Ava Chen",
        "subject": "string"
      },
      "name": "Ava Chen",
      "overdraft_currency": "string",
      "overdraft_price": 1,
      "paid_email_qty": 1,
      "send_date": "string",
      "statistics": {
        "delivered": 1,
        "error": 1,
        "link_redirected": 1,
        "opening": 1,
        "sent": 1,
        "unsubscribe": 1
      },
      "status": 1,
      "tariff_email_qty": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `all_email_qty` | number |  |
| `company_price` | string |  |
| `id` | number |  |
| `is_sms` | boolean |  |
| `is_viber` | boolean |  |
| `message` | object |  |
| `message.attachments` | string |  |
| `message.list_id` | number |  |
| `message.sender_email` | string |  |
| `message.sender_name` | string |  |
| `message.subject` | string |  |
| `name` | string |  |
| `overdraft_currency` | string |  |
| `overdraft_price` | number |  |
| `paid_email_qty` | number |  |
| `send_date` | string |  |
| `statistics` | object |  |
| `statistics.delivered` | number |  |
| `statistics.error` | number |  |
| `statistics.link_redirected` | number |  |
| `statistics.opening` | number |  |
| `statistics.sent` | number |  |
| `statistics.unsubscribe` | number |  |
| `status` | number |  |
| `tariff_email_qty` | number |  |

## Native endpoint

Through the native SendPulse API, this operation is `GET /campaigns` (base URL `https://api.sendpulse.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-campaigns.md) for the provider-specific parameters and requirements.

