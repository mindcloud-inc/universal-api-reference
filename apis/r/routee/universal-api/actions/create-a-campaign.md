# Routee: Create a campaign

Creates a new campaign in Routee.

```
POST https://connect.mindcloud.co/v1/universal/routee/latest/actions/create-a-campaign
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Routee `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/routee/latest/actions/create-a-campaign" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/routee/latest/actions/create-a-campaign', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `senderName` | string | no | Sender name |
| `senderEmail` | string | no | Sender email address |
| `subject` | string | no | Email subject |
| `body` | string | no | The email body, encoded in base64 |
| `listId` | string | no | Mailing list ID |
| `name` | string | no | Campaign name (an optional parameter) |
| `type` | string | no | Possible value - "draft" (a newsletter will be created as a draft). An optional parameter. |
| `attachments` | string | no | Attached files, a serialized array in which the key is the name of the attachment, and the value is the content of the attachment (an optional parameter) |

## Response

```json
{
  "success": true,
  "data": [
    {
      "count": "string",
      "id": "string",
      "ovedraft_currency": "string",
      "overdraft_price": "string",
      "paid_email_qty": "ava@example.com",
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
| `count` | string |  |
| `id` | string |  |
| `ovedraft_currency` | string |  |
| `overdraft_price` | string |  |
| `paid_email_qty` | string |  |
| `status` | string |  |
| `tariff_email_qty` | string |  |

## Native endpoint

Through the native Routee API, this operation is `POST /campaigns` (base URL `https://connect.routee.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-a-campaign.md) for the provider-specific parameters and requirements.

