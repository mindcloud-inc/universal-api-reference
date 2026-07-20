# Social Intents: List Chats By Date Range

Retrieves chats from Social Intents using a date range.

```
GET https://connect.mindcloud.co/v1/universal/socialIntents/latest/actions/list-chats-by-date-range
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Social Intents `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/socialIntents/latest/actions/list-chats-by-date-range?connectionId=$CONNECTION_ID&dateFrom=2025-01-01&dateTo=2025-01-31" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "dateFrom": "2025-01-01",
  "dateTo": "2025-01-31"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/socialIntents/latest/actions/list-chats-by-date-range?${params}`, {
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
| `dateFrom` | string | yes | Start date in YYYY-MM-DD format. Example: `2025-01-01`. |
| `dateTo` | string | yes | End date in YYYY-MM-DD format. Example: `2025-01-31`. |
| `timezone` | string | no | Timezone used when filtering by date range. Example: `America/New_York`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "apiStatus": "string",
      "apiStatusCode": "string",
      "apiStatusMessage": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `apiStatus` | string |  |
| `apiStatusCode` | string |  |
| `apiStatusMessage` | string |  |

## Native endpoint

Through the native Social Intents API, this operation is `GET /chats` (base URL `https://www.socialintents.com/v1/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-chats-by-date-range.md) for the provider-specific parameters and requirements.

