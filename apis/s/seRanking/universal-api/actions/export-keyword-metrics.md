# SE Ranking Data: Export keyword metrics

Exports keyword metrics from SE Ranking Data.

```
GET https://connect.mindcloud.co/v1/universal/seRanking/latest/actions/export-keyword-metrics
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SE Ranking Data `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/seRanking/latest/actions/export-keyword-metrics?connectionId=$CONNECTION_ID&keywords=string&source=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "keywords": "string",
  "source": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/seRanking/latest/actions/export-keyword-metrics?${params}`, {
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
| `cols` | string | no | Comma-separated fields to include in the export response. |
| `keywords` | list<string> | yes | List of keywords to export metrics for. |
| `sort` | list<string> | no | Optional sort field (for example: cpc). One of: `competition`, `cpc`, `difficulty`, `volume`. |
| `sortOrder` | list<string> | no | Optional sort order (asc or desc). One of: `asc`, `desc`. |
| `source` | string | yes | Regional database code (for example: us). |

## Response

```json
{
  "success": true,
  "data": [
    {
      "competition": 1,
      "cpc": 1,
      "difficulty": 1,
      "isDataFound": true,
      "keyword": "string",
      "volume": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `competition` | number |  |
| `cpc` | number |  |
| `difficulty` | number |  |
| `isDataFound` | boolean |  |
| `keyword` | string |  |
| `volume` | number |  |

## Native endpoint

Through the native SE Ranking Data API, this operation is `POST /keywords/export` (base URL `https://api.seranking.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/export-keyword-metrics.md) for the provider-specific parameters and requirements.

