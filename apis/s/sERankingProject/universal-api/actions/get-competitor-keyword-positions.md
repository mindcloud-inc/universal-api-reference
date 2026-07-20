# SE Ranking Project: Get Competitor Keyword Positions

Retrieves competitor keyword rankings from SE Ranking.

```
GET https://connect.mindcloud.co/v1/universal/sERankingProject/latest/actions/get-competitor-keyword-positions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SE Ranking Project `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sERankingProject/latest/actions/get-competitor-keyword-positions?connectionId=$CONNECTION_ID&competitor_id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "competitor_id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sERankingProject/latest/actions/get-competitor-keyword-positions?${params}`, {
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
| `competitor_id` | number | yes |  |
| `date_from` | date | no |  |
| `date_to` | date | no |  |
| `site_engine_id` | number | no |  |
| `with_serp_features` | number | no |  |

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

Through the native SE Ranking Project API, this operation is `GET /competitors/:competitor_id/positions` (base URL `https://api4.seranking.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-competitor-keyword-positions.md) for the provider-specific parameters and requirements.

