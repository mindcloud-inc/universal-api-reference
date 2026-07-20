# Usedesk: Get Ticket

Retrieves a ticket by ID from Usedesk.

```
GET https://connect.mindcloud.co/v1/universal/usedesk/latest/actions/get-ticket
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Usedesk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/usedesk/latest/actions/get-ticket?connectionId=$CONNECTION_ID&ticketId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "ticketId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/usedesk/latest/actions/get-ticket?${params}`, {
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
| `ticketId` | number | yes | Ticket ID. |
| `accessibleForAgentId` | number | no | Agent ID used to evaluate access rights for the ticket. |
| `properties[]` | array<string> | no | Additional ticket properties to include, such as SLA values. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "changes": [
        {}
      ],
      "comments": [
        {}
      ],
      "custom_fields": [
        {}
      ],
      "tags": [
        {}
      ],
      "ticket": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `changes` | array<object> |  |
| `comments` | array<object> |  |
| `custom_fields` | array<object> |  |
| `tags` | array<object> |  |
| `ticket` | object |  |

## Native endpoint

Through the native Usedesk API, this operation is `POST /ticket` (base URL `https://secure.usedesk.com/uapi`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-ticket.md) for the provider-specific parameters and requirements.

