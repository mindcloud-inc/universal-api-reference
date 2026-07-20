# Ahrefs: Get Domain Rating



```
GET https://connect.mindcloud.co/v1/universal/ahrefs/latest/actions/get-domain-rating
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ahrefs `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ahrefs/latest/actions/get-domain-rating?connectionId=$CONNECTION_ID&target=string&date=2026-05-07T12%3A00%3A00.000Z" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "target": "string",
  "date": "2026-05-07T12:00:00.000Z"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ahrefs/latest/actions/get-domain-rating?${params}`, {
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
| `target` | string | yes | Domain or URL to analyze. |
| `date` | date | yes | Report date in YYYY-MM-DD format. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "ahrefsRank": 1,
      "domainRating": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `ahrefsRank` | number | The target's Ahrefs rank, where rank #1 is the strongest backlink profile. |
| `domainRating` | number | The target's Domain Rating score on Ahrefs' 100-point logarithmic scale. |

## Native endpoint

Through the native Ahrefs API, this operation is `GET /site-explorer/domain-rating` (base URL `https://api.ahrefs.com/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-domain-rating.md) for the provider-specific parameters and requirements.

