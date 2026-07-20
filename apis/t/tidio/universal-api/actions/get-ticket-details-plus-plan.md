# Tidio: Get Ticket Details [Plus plan]

Retrieves ticket details from the Tidio workspace.

```
GET https://connect.mindcloud.co/v1/universal/tidio/latest/actions/get-ticket-details-plus-plan
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Tidio `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tidio/latest/actions/get-ticket-details-plus-plan?connectionId=$CONNECTION_ID&ticketId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "ticketId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/tidio/latest/actions/get-ticket-details-plus-plan?${params}`, {
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
| `ticketId` | string | yes | The Tidio ticket ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "assignedDepartmentId": "string",
      "assignedOperatorId": "string",
      "contactEmail": "ava@example.com",
      "contactId": "string",
      "customChannelId": "string",
      "id": 1,
      "link": "https://example.com",
      "messages": [
        "string"
      ],
      "priority": "string",
      "status": "string",
      "subject": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `assignedDepartmentId` | string | ID of assigned Department |
| `assignedOperatorId` | string | ID of assigned Operator |
| `contactEmail` | string | Email of contact where ticket messages are sent |
| `contactId` | string | ID of the contact |
| `customChannelId` | string | ID of custom channel attached to given ticket. |
| `id` | number | Ticket ID |
| `link` | string | URL to ticket |
| `messages` | array<string> |  |
| `priority` | string | Ticket priority |
| `status` | string | Ticket status |
| `subject` | string | Ticket subject |

## Native endpoint

Through the native Tidio API, this operation is `GET /tickets/{ticketId}` (base URL `https://api.tidio.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-ticket-details-plus-plan.md) for the provider-specific parameters and requirements.

