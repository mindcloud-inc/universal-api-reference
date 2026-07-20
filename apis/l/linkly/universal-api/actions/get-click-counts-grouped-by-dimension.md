# Linkly: Get Click Counts Grouped By Dimension

Retrieves click counts by dimension from Linkly.

```
GET https://connect.mindcloud.co/v1/universal/linkly/latest/actions/get-click-counts-grouped-by-dimension
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Linkly `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/linkly/latest/actions/get-click-counts-grouped-by-dimension?connectionId=$CONNECTION_ID&counter=country" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "counter": "country"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/linkly/latest/actions/get-click-counts-grouped-by-dimension?${params}`, {
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
| `counter` | list | yes | The dimension to group clicks by. One of: `country`, `isp`, `link_id`, `platform`, `referer`, `top_params`. |
| `link_id` | number | no | The id of a single Link. |
| `start` | string | no | The start date for the date range. Example: `2026-03-24`. |
| `end` | string | no | The end date for the date range. Example: `2026-03-24`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `link_ids` | string | no | Comma-separated list of Link IDs. Example: `39187500,39187501`. |
| `country` | string | no | Filter by country using ISO 3166-1 alpha-2 country code. Example: `US`. |
| `bots` | boolean | no | Set to false to exclude bot clicks from the results. |
| `unique` | boolean | no | Set to true to only count unique clicks. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "total": 1,
      "values": [
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
| `total` | number | Total click count across the selected grouping. |
| `values` | array<object> | Grouped counter rows with value and count. |

## Native endpoint

Through the native Linkly API, this operation is `GET /workspace/:workspace_id/clicks/counters/:counter` (base URL `https://app.linklyhq.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-click-counts-grouped-by-dimension.md) for the provider-specific parameters and requirements.

