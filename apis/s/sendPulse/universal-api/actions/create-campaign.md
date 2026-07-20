# SendPulse: Create Campaign

Creates a new campaign in SendPulse.

```
POST https://connect.mindcloud.co/v1/universal/sendPulse/latest/actions/create-campaign
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SendPulse `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/sendPulse/latest/actions/create-campaign" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "March Newsletter Draft",
  "subject": "March Product Update",
  "senderName": "MindCloud Team",
  "senderEmail": "updates@example.com",
  "mailingListId": "123456"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/sendPulse/latest/actions/create-campaign', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "March Newsletter Draft",
    "subject": "March Product Update",
    "senderName": "MindCloud Team",
    "senderEmail": "updates@example.com",
    "mailingListId": "123456"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | Name of the campaign. Example: `March Newsletter Draft`. |
| `subject` | string | yes | Email subject line. Example: `March Product Update`. |
| `senderName` | string | yes | Display name of the sender. Example: `MindCloud Team`. |
| `senderEmail` | string | yes | Verified sender email address. Example: `updates@example.com`. |
| `mailingListId` | string | yes | Mailing list used for the campaign. Example: `123456`. |
| `body` | string | no | Base64-encoded HTML body for the campaign. Provide this or Template ID. Example: `PGgxPkNhbXBhaWduIEJvZHk8L2gxPg==`. |
| `templateId` | string | no | Template used to render the campaign. Provide this or HTML Body Base64. Example: `345678`. |
| `type` | string | no | Use draft to create safely before scheduling or sending. Default: `draft`. Example: `draft`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `sendDate` | string | no | Optional scheduled send date and time. Requires active emails in the mailing list. Example: `2026-03-20 10:00:00`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "count": 1,
      "id": 1,
      "overdraft_currency": "string",
      "overdraft_price": "string",
      "paid_email_qty": 1,
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
| `count` | number |  |
| `id` | number |  |
| `overdraft_currency` | string |  |
| `overdraft_price` | string |  |
| `paid_email_qty` | number |  |
| `status` | number |  |
| `tariff_email_qty` | number |  |

## Native endpoint

Through the native SendPulse API, this operation is `POST /campaigns` (base URL `https://api.sendpulse.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-campaign.md) for the provider-specific parameters and requirements.

