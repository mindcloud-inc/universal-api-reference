# Deskpro: Get Ticket Filter

Retrieves a ticket filter from Deskpro.

```
GET https://connect.mindcloud.co/v1/universal/deskpro/latest/actions/get-ticket-filter
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Deskpro `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/deskpro/latest/actions/get-ticket-filter?connectionId=$CONNECTION_ID&ticketFilterId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "ticketFilterId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/deskpro/latest/actions/get-ticket-filter?${params}`, {
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
      "id": 1,
      "isEnabled": true,
      "isGlobal": true,
      "query": "string",
      "sharedAgents": [
        1
      ],
      "sharedTeams": [
        1
      ],
      "title": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | number |  |
| `isEnabled` | boolean |  |
| `isGlobal` | boolean |  |
| `query` | string |  |
| `sharedAgents[]` | number |  |
| `sharedTeams[]` | number |  |
| `title` | string |  |

## Native endpoint

Through the native Deskpro API, this operation is `GET /ticket_filters/:ticketFilterId` (base URL `{{credentials.helpdeskUrl}}/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-ticket-filter.md) for the provider-specific parameters and requirements.

