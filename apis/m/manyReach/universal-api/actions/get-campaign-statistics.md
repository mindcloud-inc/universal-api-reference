# ManyReach: Get Campaign Statistics

Retrieves campaign statistics from ManyReach.

```
GET https://connect.mindcloud.co/v1/universal/manyReach/latest/actions/get-campaign-statistics
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ManyReach `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/manyReach/latest/actions/get-campaign-statistics?connectionId=$CONNECTION_ID&id=123" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "123"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/manyReach/latest/actions/get-campaign-statistics?${params}`, {
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
| `id` | number | yes | Campaign ID for which statistics are retrieved. Example: `123`. |
| `dateStart` | date | no | Start date for the statistics range. Example: `2026-03-01T00:00:00Z`. |
| `dateEnd` | date | no | End date for the statistics range. Example: `2026-03-24T23:59:59Z`. |
| `refresh` | boolean | no | Force-refresh campaign statistics before retrieval. Default: `false`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "campaignId": 1,
      "clicksSeries": {},
      "followupStats": [
        {}
      ],
      "opensSeries": {},
      "replySeries": {},
      "sentInitialSeries": {},
      "sentSeries": {},
      "timeline": [
        "2026-05-07T12:00:00.000Z"
      ],
      "unspamSeries": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `campaignId` | number | Unique identifier of the campaign. |
| `clicksSeries` | object | Link clicks per time period. |
| `followupStats` | array<object> | Breakdown of statistics by individual followup emails. |
| `opensSeries` | object | Email opens per time period. |
| `replySeries` | object | Replies received per time period. |
| `sentInitialSeries` | object | Initial messages sent per time period. |
| `sentSeries` | object | Total messages sent per time period. |
| `timeline` | array<date> | Common timeline for all series data points. |
| `unspamSeries` | object | Unspam or unsubscribe actions per time period. |

## Native endpoint

Through the native ManyReach API, this operation is `GET https://api.manyreach.com/api/v2/campaigns/:id/stats` (base URL `https://api.manyreach.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-campaign-statistics.md) for the provider-specific parameters and requirements.

