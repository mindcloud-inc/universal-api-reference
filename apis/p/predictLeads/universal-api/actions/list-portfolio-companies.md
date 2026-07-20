# PredictLeads: List Portfolio Companies

Retrieves portfolio companies from the PredictLeads API.

```
GET https://connect.mindcloud.co/v1/universal/predictLeads/latest/actions/list-portfolio-companies
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PredictLeads `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/predictLeads/latest/actions/list-portfolio-companies?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/predictLeads/latest/actions/list-portfolio-companies?${params}`, {
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
| `firstSeenAtFrom` | string | no | Include portfolio-company connections first seen on or after this date. Example: `2024-01-01`. |
| `firstSeenAtUntil` | string | no | Include portfolio-company connections first seen on or before this date. Example: `2024-12-31`. |
| `lastSeenAtFrom` | string | no | Include portfolio-company connections last seen on or after this date. Example: `2024-01-01`. |
| `lastSeenAtUntil` | string | no | Include portfolio-company connections last seen on or before this date. Example: `2024-12-31`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native PredictLeads API returns.

## Native endpoint

Through the native PredictLeads API, this operation is `GET /discover/portfolio_companies/connections` (base URL `https://predictleads.com/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-portfolio-companies.md) for the provider-specific parameters and requirements.

