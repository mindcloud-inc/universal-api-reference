# SendPulse: Get Campaign Information

Retrieves a campaign from SendPulse by ID.

```
GET https://connect.mindcloud.co/v1/universal/sendPulse/latest/actions/get-campaign-information
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SendPulse `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sendPulse/latest/actions/get-campaign-information?connectionId=$CONNECTION_ID&campaignId=987654" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "campaignId": "987654"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sendPulse/latest/actions/get-campaign-information?${params}`, {
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
| `campaignId` | string | yes | The SendPulse campaign identifier. Example: `987654`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "all_email_qty": 1,
      "company_price": "string",
      "external_stat": {
        "check_open_email": true,
        "check_redirect_link": true
      },
      "id": 1,
      "is_sms": true,
      "is_viber": true,
      "message": {
        "attachments": "string",
        "body": "string",
        "list_id": 1,
        "preheader": "string",
        "sender_email": "ava@example.com",
        "sender_name": "Ava Chen",
        "subject": "string"
      },
      "name": "Ava Chen",
      "overdraft_currency": "string",
      "overdraft_price": 1,
      "paid_email_qty": 1,
      "permalink": "https://example.com",
      "send_date": "string",
      "statistics": {
        "clicks": [
          [
            "string"
          ]
        ],
        "general": [
          [
            {}
          ]
        ]
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
| `external_stat` | object |  |
| `external_stat.check_open_email` | boolean |  |
| `external_stat.check_redirect_link` | boolean |  |
| `id` | number |  |
| `is_sms` | boolean |  |
| `is_viber` | boolean |  |
| `message` | object |  |
| `message.attachments` | string |  |
| `message.body` | string |  |
| `message.list_id` | number |  |
| `message.preheader` | string |  |
| `message.sender_email` | string |  |
| `message.sender_name` | string |  |
| `message.subject` | string |  |
| `name` | string |  |
| `overdraft_currency` | string |  |
| `overdraft_price` | number |  |
| `paid_email_qty` | number |  |
| `permalink` | string |  |
| `send_date` | string |  |
| `statistics` | object |  |
| `statistics.clicks[]` | array |  |
| `statistics.general[]` | array<object> |  |
| `statistics.general[].code` | number |  |
| `statistics.general[].count` | number |  |
| `statistics.general[].explain` | string |  |
| `status` | number |  |
| `tariff_email_qty` | number |  |

## Native endpoint

Through the native SendPulse API, this operation is `GET /campaigns/:campaignId` (base URL `https://api.sendpulse.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-campaign-information.md) for the provider-specific parameters and requirements.

