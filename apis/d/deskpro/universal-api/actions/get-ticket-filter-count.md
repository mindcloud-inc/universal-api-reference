# Deskpro: Get Ticket Filter Count

Retrieves the ticket count for a Deskpro filter.

```
GET https://connect.mindcloud.co/v1/universal/deskpro/latest/actions/get-ticket-filter-count
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Deskpro `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/deskpro/latest/actions/get-ticket-filter-count?connectionId=$CONNECTION_ID&ticketFilterId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "ticketFilterId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/deskpro/latest/actions/get-ticket-filter-count?${params}`, {
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
| `ticketFilterId` | number | yes | Example: `1`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "count": 1,
      "groupedBy": "string",
      "id": 1,
      "title": "string",
      "type": "string",
      "value": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `count` | number |  |
| `groupedBy` | string |  |
| `id` | number |  |
| `title` | string |  |
| `type` | string |  |
| `value` | string |  |

## Native endpoint

Through the native Deskpro API, this operation is `GET /ticket_filters/:ticketFilterId/count` (base URL `{{credentials.helpdeskUrl}}/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-ticket-filter-count.md) for the provider-specific parameters and requirements.

