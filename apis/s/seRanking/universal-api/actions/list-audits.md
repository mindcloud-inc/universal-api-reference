# SE Ranking Data: List audits

Retrieves a list of audits from SE Ranking Data.

```
GET https://connect.mindcloud.co/v1/universal/seRanking/latest/actions/list-audits
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SE Ranking Data `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/seRanking/latest/actions/list-audits?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/seRanking/latest/actions/list-audits?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "items": [
        {
          "groupId": 1,
          "hasProject": true,
          "id": 1,
          "isNew": 1,
          "ownerAccountId": 1,
          "stats": {
            "crawled": 1,
            "errors": 1,
            "notices": 1,
            "score": 1,
            "warnings": 1
          },
          "status": "string",
          "title": "string",
          "url": "https://example.com",
          "version": "string"
        }
      ],
      "total": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `items` | array<object> |  |
| `items[].groupId` | number |  |
| `items[].hasProject` | boolean |  |
| `items[].id` | number |  |
| `items[].isNew` | number |  |
| `items[].ownerAccountId` | number |  |
| `items[].stats` | object |  |
| `items[].stats.crawled` | number |  |
| `items[].stats.errors` | number |  |
| `items[].stats.notices` | number |  |
| `items[].stats.score` | number |  |
| `items[].stats.warnings` | number |  |
| `items[].status` | string |  |
| `items[].title` | string |  |
| `items[].url` | string |  |
| `items[].version` | string |  |
| `total` | number |  |

## Native endpoint

Through the native SE Ranking Data API, this operation is `GET /site-audit/audits` (base URL `https://api.seranking.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-audits.md) for the provider-specific parameters and requirements.

