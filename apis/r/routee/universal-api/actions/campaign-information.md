# Routee: Campaign information

Retrieves detailed campaign information from Routee.

```
GET https://connect.mindcloud.co/v1/universal/routee/latest/actions/campaign-information
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Routee `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/routee/latest/actions/campaign-information?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/routee/latest/actions/campaign-information?${params}`, {
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
| `id` | string | yes | Campaign ID |

## Response

```json
{
  "success": true,
  "data": [
    {
      "all_email_qty": 1,
      "id": "string",
      "message": {
        "attachments": "string",
        "list_id": "string",
        "sender_email": "ava@example.com",
        "sender_name": "Ava Chen",
        "subject": "string"
      },
      "name": "Ava Chen",
      "overdraft_currency": "string",
      "overdraft_price": 1,
      "paid_email_qty": "ava@example.com",
      "statistics": [
        [
          {}
        ]
      ],
      "status": "string",
      "tariff_email_qty": "ava@example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `all_email_qty` | number |  |
| `id` | string |  |
| `message` | object |  |
| `message.attachments` | string |  |
| `message.list_id` | string |  |
| `message.sender_email` | string |  |
| `message.sender_name` | string |  |
| `message.subject` | string |  |
| `name` | string |  |
| `overdraft_currency` | string |  |
| `overdraft_price` | number |  |
| `paid_email_qty` | string |  |
| `statistics[]` | array<object> |  |
| `statistics[].code` | number |  |
| `statistics[].count` | number |  |
| `statistics[].explain` | string |  |
| `status` | string |  |
| `tariff_email_qty` | string |  |

## Native endpoint

Through the native Routee API, this operation is `GET /campaigns/:id` (base URL `https://connect.routee.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/campaign-information.md) for the provider-specific parameters and requirements.

