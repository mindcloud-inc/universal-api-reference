# SE Ranking Data: List all backlinks

Retrieves all backlinks from SE Ranking Data.

```
GET https://connect.mindcloud.co/v1/universal/seRanking/latest/actions/list-all-backlinks
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SE Ranking Data `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/seRanking/latest/actions/list-all-backlinks?connectionId=$CONNECTION_ID&target=seranking.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "target": "seranking.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/seRanking/latest/actions/list-all-backlinks?${params}`, {
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
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `backlinks` | array<object> | Backlink rows. |
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

## Native endpoint

Through the native SE Ranking Data API, this operation is `GET /backlinks/all` (base URL `https://api.seranking.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-all-backlinks.md) for the provider-specific parameters and requirements.

