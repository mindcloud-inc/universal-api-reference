# Geral: Get Link Statistics

Retrieves statistics for a link in Geral.

```
GET https://connect.mindcloud.co/v1/universal/geral/latest/actions/get-link-statistics
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Geral `connectionId` ([setup](../authentication.md)).

This action also supports [filtering](../filtering.md) (`where`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/geral/latest/actions/get-link-statistics?connectionId=$CONNECTION_ID&linkId=1&startDate=string&endDate=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "linkId": "1",
  "startDate": "string",
  "endDate": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/geral/latest/actions/get-link-statistics?${params}`, {
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
| `linkId` | number | yes | The link ID to retrieve statistics for. |
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

Through the native Geral API, this operation is `GET /statistics/:link_id` (base URL `https://ger.al/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-link-statistics.md) for the provider-specific parameters and requirements.

