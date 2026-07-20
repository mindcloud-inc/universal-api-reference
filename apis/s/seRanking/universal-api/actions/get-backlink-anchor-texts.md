# SE Ranking Data: Get backlink anchor texts

Retrieves backlink anchor texts from SE Ranking Data.

```
GET https://connect.mindcloud.co/v1/universal/seRanking/latest/actions/get-backlink-anchor-texts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SE Ranking Data `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/seRanking/latest/actions/get-backlink-anchor-texts?connectionId=$CONNECTION_ID&target=seranking.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "target": "seranking.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/seRanking/latest/actions/get-backlink-anchor-texts?${params}`, {
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
      "anchors": [
        {
          "anchor": "string",
          "backlinks": 1,
          "dofollowBacklinks": 1,
          "firstSeen": "string",
          "lastVisited": "string",
          "nofollowBacklinks": 1,
          "refdomains": 1
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
| `anchors` | array<object> | Anchor text rows. |
| `anchors[].anchor` | string |  |
| `anchors[].backlinks` | number |  |
| `anchors[].dofollowBacklinks` | number |  |
| `anchors[].firstSeen` | string |  |
| `anchors[].lastVisited` | string |  |
| `anchors[].nofollowBacklinks` | number |  |
| `anchors[].refdomains` | number |  |

## Native endpoint

Through the native SE Ranking Data API, this operation is `GET /backlinks/anchors` (base URL `https://api.seranking.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-backlink-anchor-texts.md) for the provider-specific parameters and requirements.

