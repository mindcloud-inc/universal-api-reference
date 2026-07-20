# Octanist: Get Stats

Retrieves dashboard statistics from Octanist.

```
GET https://connect.mindcloud.co/v1/universal/octanist/latest/actions/get-stats
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Octanist `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/octanist/latest/actions/get-stats?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/octanist/latest/actions/get-stats?${params}`, {
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
| `period` | string | no | Time period to query: current, previous, or custom. Default: `current`. |
| `startDate` | string | no | Start date in YYYY-MM-DD format when period is custom. Example: `2026-03-01`. |
| `endDate` | string | no | End date in YYYY-MM-DD format when period is custom. Example: `2026-03-25`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Octanist API returns.

## Native endpoint

Through the native Octanist API, this operation is `POST /stats` (base URL `https://octanist.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-stats.md) for the provider-specific parameters and requirements.

