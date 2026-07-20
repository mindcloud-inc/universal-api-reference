# Zendesk: List Ticket Forms

Retrieves a list of Zendesk ticket forms.

```
GET https://connect.mindcloud.co/v1/universal/zendesk/latest/actions/list-ticket-forms
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zendesk `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zendesk/latest/actions/list-ticket-forms?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zendesk/latest/actions/list-ticket-forms?${params}`, {
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
      "createdAt": "2026-05-07T12:00:00.000Z",
      "default": true,
      "displayName": "Ava Chen",
      "endUserVisible": true,
      "id": 1,
      "inAllBrands": true,
      "name": "Ava Chen",
      "position": 1,
      "ticketFieldIds": [
        1
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
| `active` | boolean | Whether the ticket form is active. |
| `createdAt` | date | Creation timestamp. |
| `default` | boolean | Whether this is the default ticket form. |
| `displayName` | string | Display name of the ticket form. |
| `endUserVisible` | boolean | Whether the form is visible to end users. |
| `id` | number | Ticket form id. |
| `inAllBrands` | boolean | Whether the form is available in all brands. |
| `name` | string | Internal ticket form name. |
| `position` | number | Display position of the ticket form. |
| `ticketFieldIds[]` | number | Ticket field ids included in the form. |
| `updatedAt` | date | Last update timestamp. |
| `url` | string | URL of the ticket form resource. |

## Native endpoint

Through the native Zendesk API, this operation is `GET /ticket_forms.json` (base URL `https://{{credentials.subdomain}}.zendesk.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-ticket-forms.md) for the provider-specific parameters and requirements.

