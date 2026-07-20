# Social Intents: List Contacts By Date Range

Retrieves contacts from Social Intents using a date range.

```
GET https://connect.mindcloud.co/v1/universal/socialIntents/latest/actions/list-contacts-by-date-range
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Social Intents `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/socialIntents/latest/actions/list-contacts-by-date-range?connectionId=$CONNECTION_ID&dateFrom=2026-03-01&dateTo=2026-03-31" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "dateFrom": "2026-03-01",
  "dateTo": "2026-03-31"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/socialIntents/latest/actions/list-contacts-by-date-range?${params}`, {
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
| `dateFrom` | string | yes | Start date for contact filtering. Example: `2026-03-01`. |
| `dateTo` | string | yes | End date for contact filtering. Example: `2026-03-31`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Social Intents API returns.

## Native endpoint

Through the native Social Intents API, this operation is `GET /contacts` (base URL `https://www.socialintents.com/v1/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-contacts-by-date-range.md) for the provider-specific parameters and requirements.

