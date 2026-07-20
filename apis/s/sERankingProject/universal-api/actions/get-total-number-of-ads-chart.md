# SE Ranking Project: Get Total Number Of Ads Chart

Retrieves keyword ad counts by date from SE Ranking.

```
GET https://connect.mindcloud.co/v1/universal/sERankingProject/latest/actions/get-total-number-of-ads-chart
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SE Ranking Project `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sERankingProject/latest/actions/get-total-number-of-ads-chart?connectionId=$CONNECTION_ID&date_from=2026-05-07T12%3A00%3A00.000Z&date_to=2026-05-07T12%3A00%3A00.000Z&site_id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "date_from": "2026-05-07T12:00:00.000Z",
  "date_to": "2026-05-07T12:00:00.000Z",
  "site_id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sERankingProject/latest/actions/get-total-number-of-ads-chart?${params}`, {
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
| `date_from` | date | yes |  |
| `date_to` | date | yes |  |
| `keywordIds[]` | array<number> | no |  |
| `site_id` | list<number> | yes |  |
| `siteEngineIds[]` | array<number> | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "value": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `value` | array | The raw response body. The saved successful response was an empty array (HTTP 200). |

## Native endpoint

Through the native SE Ranking Project API, this operation is `GET /sites/:site_id/ads` (base URL `https://api4.seranking.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-total-number-of-ads-chart.md) for the provider-specific parameters and requirements.

