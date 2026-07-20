# Deskpro: List Ticket Filters

Retrieves a list of ticket filters from Deskpro.

```
GET https://connect.mindcloud.co/v1/universal/deskpro/latest/actions/list-ticket-filters
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Deskpro `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/deskpro/latest/actions/list-ticket-filters?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/deskpro/latest/actions/list-ticket-filters?${params}`, {
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

Through the native Deskpro API, this operation is `GET /ticket_filters` (base URL `{{credentials.helpdeskUrl}}/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-ticket-filters.md) for the provider-specific parameters and requirements.

