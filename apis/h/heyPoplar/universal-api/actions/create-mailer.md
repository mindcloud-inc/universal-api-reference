# HeyPoplar: Create Mailer

Creates a new mailer in HeyPoplar.

```
POST https://connect.mindcloud.co/v1/universal/heyPoplar/latest/actions/create-mailer
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a HeyPoplar `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/heyPoplar/latest/actions/create-mailer" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "campaignId": "string",
  "recipient.address1": "string",
  "recipient.city": "string",
  "recipient.state": "string",
  "recipient.postalCode": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/heyPoplar/latest/actions/create-mailer', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "campaignId": "string",
    "recipient.address1": "string",
    "recipient.city": "string",
    "recipient.state": "string",
    "recipient.postalCode": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `campaignId` | string | yes | ID of the campaign to use for the mailing. |
| `creativeId` | string | no | Optional creative ID. If omitted, Poplar uses the default creative. |
| `sendAt` | string | no | Future ISO8601 timestamp for when the mailing should be sent. |
| `recipient.fullName` | string | no | Optional recipient name. Poplar uses Current Resident if omitted. |
| `recipient.email` | string | no | Optional recipient email address. |
| `recipient.address1` | string | yes | Recipient street address. |
| `recipient.city` | string | yes | Recipient city. |
| `recipient.state` | string | yes | Recipient state abbreviation. |
| `recipient.postalCode` | string | yes | Recipient postal code. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "back_url": "https://example.com",
      "creative_id": "string",
      "front_url": "https://example.com",
      "id": "string",
      "pdf_url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `back_url` | string | Public URL to the back preview image from the official Poplar mailing response example. |
| `creative_id` | string | Creative identifier from the official Poplar mailing response example. |
| `front_url` | string | Public URL to the front preview image from the official Poplar mailing response example. |
| `id` | string | Mailer identifier from the official Poplar mailing response example. |
| `pdf_url` | string | Public URL to the PDF preview from the official Poplar mailing response example. |

## Native endpoint

Through the native HeyPoplar API, this operation is `POST /mailing` (base URL `https://api.heypoplar.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-mailer.md) for the provider-specific parameters and requirements.

