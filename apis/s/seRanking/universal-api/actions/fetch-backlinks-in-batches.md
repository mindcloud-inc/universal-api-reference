# SE Ranking Data: Fetch backlinks in batches

Retrieves backlinks in batches from SE Ranking Data.

```
GET https://connect.mindcloud.co/v1/universal/seRanking/latest/actions/fetch-backlinks-in-batches
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SE Ranking Data `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/seRanking/latest/actions/fetch-backlinks-in-batches?connectionId=$CONNECTION_ID&target=seranking.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "target": "seranking.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/seRanking/latest/actions/fetch-backlinks-in-batches?${params}`, {
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
      "backlinks": [
        {
          "alt": "https://example.com",
          "anchor": "https://example.com",
          "domainInlinkRank": 1,
          "firstSeen": "https://example.com",
          "image": true,
          "imageSource": "https://example.com",
          "inlinkRank": 1,
          "lastVisited": "https://example.com",
          "nofollow": true,
          "title": "https://example.com",
          "urlFrom": "https://example.com",
          "urlTo": "https://example.com"
        }
      ],
      "next": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `backlinks` | array<object> | Backlink rows for current batch. |
| `backlinks[].alt` | string |  |
| `backlinks[].anchor` | string |  |
| `backlinks[].domainInlinkRank` | number |  |
| `backlinks[].firstSeen` | string |  |
| `backlinks[].image` | boolean |  |
| `backlinks[].imageSource` | string |  |
| `backlinks[].inlinkRank` | number |  |
| `backlinks[].lastVisited` | string |  |
| `backlinks[].nofollow` | boolean |  |
| `backlinks[].title` | string |  |
| `backlinks[].urlFrom` | string |  |
| `backlinks[].urlTo` | string |  |
| `next` | string | Pagination cursor/token for next batch. |

## Native endpoint

Through the native SE Ranking Data API, this operation is `GET /backlinks/raw` (base URL `https://api.seranking.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/fetch-backlinks-in-batches.md) for the provider-specific parameters and requirements.

