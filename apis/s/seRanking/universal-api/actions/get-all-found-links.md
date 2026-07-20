# SE Ranking Data: Get all found links

Retrieves all found links from SE Ranking Data.

```
GET https://connect.mindcloud.co/v1/universal/seRanking/latest/actions/get-all-found-links
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SE Ranking Data `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/seRanking/latest/actions/get-all-found-links?connectionId=$CONNECTION_ID&auditId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "auditId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/seRanking/latest/actions/get-all-found-links?${params}`, {
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
| `auditId` | list<string> | yes | Audit identifier. Example: `1`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "items": [
        {
          "alt": "string",
          "anchorType": "string",
          "id": "string",
          "nofollow": "string",
          "sourceNoindex": "string",
          "sourceUrl": "https://example.com",
          "status": "string",
          "title": "string",
          "type": "string",
          "url": "https://example.com"
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
| `items[].alt` | string |  |
| `items[].anchorType` | string |  |
| `items[].id` | string |  |
| `items[].nofollow` | string |  |
| `items[].sourceNoindex` | string |  |
| `items[].sourceUrl` | string |  |
| `items[].status` | string |  |
| `items[].title` | string |  |
| `items[].type` | string |  |
| `items[].url` | string |  |
| `total` | number |  |

## Native endpoint

Through the native SE Ranking Data API, this operation is `GET /site-audit/audits/links` (base URL `https://api.seranking.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-all-found-links.md) for the provider-specific parameters and requirements.

