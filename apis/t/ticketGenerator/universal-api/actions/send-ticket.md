# Ticket Generator: Send Ticket

Sends a ticket by email, SMS, or WhatsApp in Ticket Generator.

```
POST https://connect.mindcloud.co/v1/universal/ticketGenerator/latest/actions/send-ticket
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ticket Generator `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/ticketGenerator/latest/actions/send-ticket" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "eventId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/ticketGenerator/latest/actions/send-ticket', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "eventId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `eventId` | string | yes | Ticket Generator event identifier. |
| `ticketCategoryId` | string | no | Ticket category identifier. Optional when the event has exactly one ticket category. |
| `email` | string | no | Recipient email address. |
| `phoneNumber` | string | no | Recipient phone number in E.164 format. |
| `whatsApp` | boolean | no | Send the ticket over WhatsApp instead of SMS when a phone number is provided. |
| `whatsAppConsent` | boolean | no | Confirms the recipient consented to receive the ticket on WhatsApp. |
| `subject` | string | no | Email subject line. |
| `body` | string | no | Email body content. |
| `fromName` | string | no | Sender name displayed in the email. |
| `header1` | string | no | Variable information field label 1. |
| `value1` | string | no | Variable information field value 1. |
| `header2` | string | no | Variable information field label 2. |
| `value2` | string | no | Variable information field value 2. |
| `header3` | string | no | Variable information field label 3. |
| `value3` | string | no | Variable information field value 3. |
| `header4` | string | no | Variable information field label 4. |
| `value4` | string | no | Variable information field value 4. |
| `header5` | string | no | Variable information field label 5. |
| `value5` | string | no | Variable information field value 5. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string",
      "mobileTicketPageLinkId": "https://example.com",
      "ticketId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string |  |
| `mobileTicketPageLinkId` | string |  |
| `ticketId` | string |  |

## Native endpoint

Through the native Ticket Generator API, this operation is `POST v1/ticket/send/` (base URL `https://apis.ticket-generator.com/client`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-ticket.md) for the provider-specific parameters and requirements.

