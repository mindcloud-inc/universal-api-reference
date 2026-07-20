# SE Ranking Data: Discover brand by URL

Discovers a brand by URL in SE Ranking Data.

```
GET https://connect.mindcloud.co/v1/universal/seRanking/latest/actions/discover-brand-by-url
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SE Ranking Data `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/seRanking/latest/actions/discover-brand-by-url?connectionId=$CONNECTION_ID&scope=base_domain&source=us&target=seranking.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "scope": "base_domain",
  "source": "us",
  "target": "seranking.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/seRanking/latest/actions/discover-brand-by-url?${params}`, {
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
| `scope` | list<string> | yes | Analysis scope (for example: base_domain). One of: `base_domain`, `domain`, `exact_url`, `path`, `subdomain`. Example: `base_domain`. |
| `source` | string | yes | Regional source code (for example: us). Example: `us`. |
| `target` | string | yes | Target domain or URL (for example: seranking.com). Example: `seranking.com`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "brands": [
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
| `brands` | array<string> | Detected brand names for the target. |

## Native endpoint

Through the native SE Ranking Data API, this operation is `GET /ai-search/discover-brand` (base URL `https://api.seranking.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/discover-brand-by-url.md) for the provider-specific parameters and requirements.

