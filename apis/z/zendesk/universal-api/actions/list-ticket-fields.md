# Zendesk: List Ticket Fields

Retrieves a list of Zendesk ticket fields.

```
GET https://connect.mindcloud.co/v1/universal/zendesk/latest/actions/list-ticket-fields
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zendesk `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zendesk/latest/actions/list-ticket-fields?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zendesk/latest/actions/list-ticket-fields?${params}`, {
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
      "active": true,
      "collapsedForAgents": true,
      "createdAt": "2026-05-07T12:00:00.000Z",
      "customFieldOptions": [
        {}
      ],
      "description": "string",
      "id": 1,
      "regexpForValidation": "string",
      "required": true,
      "title": "string",
      "type": "string",
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
| `active` | boolean | Whether the field is active. |
| `collapsedForAgents` | boolean | Whether the field is collapsed for agents. |
| `createdAt` | date | Creation timestamp. |
| `customFieldOptions[]` | object | Custom field option objects. |
| `description` | string | Ticket field description. |
| `id` | number | Ticket field id. |
| `regexpForValidation` | string | Validation expression for the field. |
| `required` | boolean | Whether the field is required. |
| `title` | string | Ticket field title. |
| `type` | string | Ticket field type. |
| `updatedAt` | date | Last update timestamp. |
| `url` | string | URL of the ticket field resource. |

## Native endpoint

Through the native Zendesk API, this operation is `GET /ticket_fields.json` (base URL `https://{{credentials.subdomain}}.zendesk.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-ticket-fields.md) for the provider-specific parameters and requirements.

