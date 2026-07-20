# Zendesk: Get Ticket

Retrieves a ticket from Zendesk.

```
GET https://connect.mindcloud.co/v1/universal/zendesk/latest/actions/get-ticket
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zendesk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zendesk/latest/actions/get-ticket?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zendesk/latest/actions/get-ticket?${params}`, {
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
| `id` | number | yes | Zendesk ticket ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "assigneeId": 1,
      "createdAt": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "groupId": 1,
      "id": 1,
      "isPublic": true,
      "organizationId": 1,
      "priority": "string",
      "requesterId": 1,
      "status": "string",
      "subject": "string",
      "tags": [
        "string"
      ],
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `assigneeId` | number |  |
| `createdAt` | date |  |
| `description` | string |  |
| `groupId` | number |  |
| `id` | number |  |
| `isPublic` | boolean |  |
| `organizationId` | number |  |
| `priority` | string |  |
| `requesterId` | number |  |
| `status` | string |  |
| `subject` | string |  |
| `tags` | array<string> |  |
| `updatedAt` | date |  |
| `url` | string |  |

## Native endpoint

Through the native Zendesk API, this operation is `GET /tickets/:id.json` (base URL `https://{{credentials.subdomain}}.zendesk.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-ticket.md) for the provider-specific parameters and requirements.

