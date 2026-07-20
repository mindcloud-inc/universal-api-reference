# Geral: List Statistics

Retrieves account statistics from Geral.

```
GET https://connect.mindcloud.co/v1/universal/geral/latest/actions/list-statistics
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Geral `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/geral/latest/actions/list-statistics?connectionId=$CONNECTION_ID&limit=25&offset=0&startDate=string&endDate=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "startDate": "string",
  "endDate": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/geral/latest/actions/list-statistics?${params}`, {
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
| `startDate` | string | yes | Start date in Y-m-d format, for example 2026-04-01. |
| `endDate` | string | yes | End date in Y-m-d format, for example 2026-04-13. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "formatted_date": "string",
      "pageviews": 1,
      "visitors": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `formatted_date` | string | Statistic period label. |
| `pageviews` | number | Pageview count. |
| `visitors` | number | Visitor count. |

## Native endpoint

Through the native Geral API, this operation is `GET /statistics/` (base URL `https://ger.al/api`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-statistics.md) for the provider-specific parameters and requirements.

