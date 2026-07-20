# Tidio: List Tickets [Plus plan]

Retrieves tickets from the Tidio workspace.

```
GET https://connect.mindcloud.co/v1/universal/tidio/latest/actions/list-tickets-plus-plan
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Tidio `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tidio/latest/actions/list-tickets-plus-plan?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/tidio/latest/actions/list-tickets-plus-plan?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "meta": {
        "cursor": "string",
        "limit": 1
      },
      "tickets": [
        {
          "assignedDepartmentId": "string",
          "assignedOperatorId": "string",
          "contactEmail": "ava@example.com",
          "contactId": "string",
          "customChannelId": "string",
          "id": 1,
          "link": "https://example.com",
          "priority": "string",
          "status": "string",
          "subject": "string"
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `meta` | object |  |
| `meta.cursor` | string | Value to fetch the next page. Null means the page is the last one. |
| `meta.limit` | number | How many items were displayed on list |
| `tickets` | array<object> |  |
| `tickets[]` | object |  |
| `tickets[].assignedDepartmentId` | string | ID of assigned Department |
| `tickets[].assignedOperatorId` | string | ID of assigned Operator |
| `tickets[].contactEmail` | string | Email of contact where ticket messages are sent |
| `tickets[].contactId` | string | ID of the contact |
| `tickets[].customChannelId` | string | ID of custom channel attached to given ticket. |
| `tickets[].id` | number | Ticket ID |
| `tickets[].link` | string | URL to ticket |
| `tickets[].priority` | string | Ticket priority |
| `tickets[].status` | string | Ticket status |
| `tickets[].subject` | string | Ticket subject |

## Native endpoint

Through the native Tidio API, this operation is `GET /tickets` (base URL `https://api.tidio.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-tickets-plus-plan.md) for the provider-specific parameters and requirements.

