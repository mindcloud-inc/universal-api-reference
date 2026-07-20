# PredictLeads: List Company News Events

Retrieves news events for a PredictLeads company.

```
GET https://connect.mindcloud.co/v1/universal/predictLeads/latest/actions/list-company-news-events
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PredictLeads `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/predictLeads/latest/actions/list-company-news-events?connectionId=$CONNECTION_ID&limit=25&offset=0&companyIdOrDomain=stripe.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "companyIdOrDomain": "stripe.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/predictLeads/latest/actions/list-company-news-events?${params}`, {
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
| `companyIdOrDomain` | string | yes | Company's ID or domain. Example: `stripe.com`. |
| `categories` | string | no | Comma-separated news event categories. Example: `funding`. |
| `foundAtFrom` | string | no | Include news events found on or after this date. Example: `2024-01-01`. |
| `foundAtUntil` | string | no | Include news events found on or before this date. Example: `2024-12-31`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native PredictLeads API returns.

## Native endpoint

Through the native PredictLeads API, this operation is `GET /companies/:company_id_or_domain/news_events` (base URL `https://predictleads.com/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-company-news-events.md) for the provider-specific parameters and requirements.

