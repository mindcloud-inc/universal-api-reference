# SE Ranking Data: Get daily count of new and lost backlinks

Retrieves daily new and lost backlink counts from SE Ranking Data.

```
GET https://connect.mindcloud.co/v1/universal/seRanking/latest/actions/get-daily-count-of-new-and-lost-backlinks
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SE Ranking Data `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/seRanking/latest/actions/get-daily-count-of-new-and-lost-backlinks?connectionId=$CONNECTION_ID&target=seranking.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "target": "seranking.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/seRanking/latest/actions/get-daily-count-of-new-and-lost-backlinks?${params}`, {
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
| `target` | string | yes | Target domain or URL to analyze (for example: seranking.com). Example: `seranking.com`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "newLostBacklinksCount": [
        {
          "date": "https://example.com",
          "lost": 1,
          "new": 1
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `newLostBacklinksCount` | array<object> | Daily new/lost backlink totals. |
| `newLostBacklinksCount[].date` | string |  |
| `newLostBacklinksCount[].lost` | number |  |
| `newLostBacklinksCount[].new` | number |  |

## Native endpoint

Through the native SE Ranking Data API, this operation is `GET /backlinks/history/count` (base URL `https://api.seranking.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-daily-count-of-new-and-lost-backlinks.md) for the provider-specific parameters and requirements.

