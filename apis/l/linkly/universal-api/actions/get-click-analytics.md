# Linkly: Get Click Analytics

Retrieves click analytics from Linkly.

```
GET https://connect.mindcloud.co/v1/universal/linkly/latest/actions/get-click-analytics
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Linkly `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/linkly/latest/actions/get-click-analytics?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/linkly/latest/actions/get-click-analytics?${params}`, {
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
| `link_id` | number | no | The id of a single Link. |
| `start` | string | no | The start date for the date range. Example: `2026-03-24`. |
| `end` | string | no | The end date for the date range. Example: `2026-03-24`. |
| `frequency` | list | no | Frequency of data points in the response. One of: `day`, `hour`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `link_ids` | string | no | Comma-separated list of Link IDs. Example: `39187500,39187501`. |
| `country` | string | no | Filter clicks by country using ISO 3166-1 alpha-2 country code. Example: `US`. |
| `browser` | string | no | Filter clicks by browser name. |
| `platform` | string | no | Filter clicks by platform or operating system. |
| `referer` | string | no | Filter clicks by referrer domain. |
| `isp` | string | no | Filter clicks by Internet Service Provider name. |
| `bots` | boolean | no | Set to false to exclude bot clicks from the results. |
| `unique` | boolean | no | Set to true to only include unique clicks in the results. |
| `timezone` | string | no | Timezone to use for date or time calculations. Example: `America/New_York`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "traffic": [
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
| `traffic` | array<object> | Time-series traffic rows with date and click count values. |

## Native endpoint

Through the native Linkly API, this operation is `GET /workspace/:workspace_id/clicks` (base URL `https://app.linklyhq.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-click-analytics.md) for the provider-specific parameters and requirements.

