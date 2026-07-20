# Ticketmaster: Find Suggest

Finds search suggestions in Ticketmaster by keyword and filters.

```
GET https://connect.mindcloud.co/v1/universal/ticketmaster/latest/actions/find-suggest
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ticketmaster `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ticketmaster/latest/actions/find-suggest?connectionId=$CONNECTION_ID&keyword=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "keyword": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ticketmaster/latest/actions/find-suggest?${params}`, {
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
| `keyword` | string | yes | Keyword to search on. |
| `size` | number | no | Maximum number of suggestion results to return. Ticketmaster allows 1 to 5 for this endpoint. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "attractions": [
        {}
      ],
      "events": [
        {}
      ],
      "venues": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `attractions` | array<object> |  |
| `events` | array<object> |  |
| `venues` | array<object> |  |

## Native endpoint

Through the native Ticketmaster API, this operation is `GET /discovery/v2/suggest.json` (base URL `https://app.ticketmaster.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/find-suggest.md) for the provider-specific parameters and requirements.

