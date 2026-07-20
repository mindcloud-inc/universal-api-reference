# Tidio: Create Ticket (As Contact) [Plus plan]

Creates a ticket as a contact in Tidio.

```
POST https://connect.mindcloud.co/v1/universal/tidio/latest/actions/create-ticket-as-contact-plus-plan
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Tidio `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/tidio/latest/actions/create-ticket-as-contact-plus-plan" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "contactEmail": "ava@example.com",
  "subject": "string",
  "messageContent": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/tidio/latest/actions/create-ticket-as-contact-plus-plan', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "contactEmail": "ava@example.com",
    "subject": "string",
    "messageContent": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `contactEmail` | string | yes | Email address of the contact creating the ticket. |
| `subject` | string | yes | Subject line of the ticket. |
| `messageContent` | string | yes | Initial message body for the ticket. |
| `assignedDepartmentId` | string | no | Optional department UUID to assign the ticket to. |
| `customChannelId` | string | no | Optional custom channel identifier used for the ticket source. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "value": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `value` | string |  |

## Native endpoint

Through the native Tidio API, this operation is `POST /tickets/as-contact` (base URL `https://api.tidio.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-ticket-as-contact-plus-plan.md) for the provider-specific parameters and requirements.

