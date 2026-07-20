# SE Ranking Data: List new and lost backlinks

Retrieves new and lost backlinks from SE Ranking Data.

```
GET https://connect.mindcloud.co/v1/universal/seRanking/latest/actions/list-new-and-lost-backlinks
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SE Ranking Data `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/seRanking/latest/actions/list-new-and-lost-backlinks?connectionId=$CONNECTION_ID&target=seranking.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "target": "seranking.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/seRanking/latest/actions/list-new-and-lost-backlinks?${params}`, {
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
      "newLostBacklinks": [
        {
          "anchor": "https://example.com",
          "domainInlinkRank": 1,
          "firstSeen": "https://example.com",
          "image": true,
          "inlinkRank": 1,
          "linkType": "https://example.com",
          "newLostDate": "https://example.com",
          "newLostType": "https://example.com",
          "nofollow": true,
          "reasonLost": "https://example.com",
          "redirectChain": true,
          "redirectChainUrls": [
            "https://example.com"
          ],
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
| `newLostBacklinks` | array<object> | New/lost backlink event rows. |
| `newLostBacklinks[].anchor` | string |  |
| `newLostBacklinks[].domainInlinkRank` | number |  |
| `newLostBacklinks[].firstSeen` | string |  |
| `newLostBacklinks[].image` | boolean |  |
| `newLostBacklinks[].inlinkRank` | number |  |
| `newLostBacklinks[].linkType` | string |  |
| `newLostBacklinks[].newLostDate` | string |  |
| `newLostBacklinks[].newLostType` | string |  |
| `newLostBacklinks[].nofollow` | boolean |  |
| `newLostBacklinks[].reasonLost` | string |  |
| `newLostBacklinks[].redirectChain` | boolean |  |
| `newLostBacklinks[].redirectChainUrls` | array<string> |  |
| `newLostBacklinks[].title` | string |  |
| `newLostBacklinks[].urlFrom` | string |  |
| `newLostBacklinks[].urlTo` | string |  |

## Native endpoint

Through the native SE Ranking Data API, this operation is `GET /backlinks/history` (base URL `https://api.seranking.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-new-and-lost-backlinks.md) for the provider-specific parameters and requirements.

