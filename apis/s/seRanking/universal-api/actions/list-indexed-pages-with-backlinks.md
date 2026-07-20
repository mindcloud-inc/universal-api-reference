# SE Ranking Data: List indexed pages with backlinks

Retrieves indexed pages with backlinks from SE Ranking Data.

```
GET https://connect.mindcloud.co/v1/universal/seRanking/latest/actions/list-indexed-pages-with-backlinks
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SE Ranking Data `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/seRanking/latest/actions/list-indexed-pages-with-backlinks?connectionId=$CONNECTION_ID&target=seranking.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "target": "seranking.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/seRanking/latest/actions/list-indexed-pages-with-backlinks?${params}`, {
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
      "pages": [
        {
          "backlinks": 1,
          "dofollowBacklinks": 1,
          "firstSeen": "string",
          "lastVisited": "string",
          "nofollowBacklinks": 1,
          "refdomains": 1,
          "url": "https://example.com"
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
| `pages` | array<object> | Indexed pages with backlinks. |
| `pages[].backlinks` | number |  |
| `pages[].dofollowBacklinks` | number |  |
| `pages[].firstSeen` | string |  |
| `pages[].lastVisited` | string |  |
| `pages[].nofollowBacklinks` | number |  |
| `pages[].refdomains` | number |  |
| `pages[].url` | string |  |

## Native endpoint

Through the native SE Ranking Data API, this operation is `GET /backlinks/indexed-pages` (base URL `https://api.seranking.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-indexed-pages-with-backlinks.md) for the provider-specific parameters and requirements.

