# SE Ranking Data: Get domain subdomains

Retrieves domain subdomains from SE Ranking Data.

```
GET https://connect.mindcloud.co/v1/universal/seRanking/latest/actions/get-domain-subdomains
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SE Ranking Data `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/seRanking/latest/actions/get-domain-subdomains?connectionId=$CONNECTION_ID&order=desc&scope=domain&sort=traffic&source=us&target=seranking.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "order": "desc",
  "scope": "domain",
  "sort": "traffic",
  "source": "us",
  "target": "seranking.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/seRanking/latest/actions/get-domain-subdomains?${params}`, {
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
| `order` | list<string> | yes | Sort order: asc or desc. One of: `asc`, `desc`. Example: `desc`. |
| `page` | string | no | Page number for pagination. Example: `1`. |
| `scope` | list<string> | yes | Analysis scope (for example: domain). One of: `base_domain`, `domain`, `exact_url`, `path`, `subdomain`. Example: `domain`. |
| `sort` | list<string> | yes | Sort field (for example: traffic, keywords_count, backlinks_count). One of: `backlinks_count`, `keywords_count`, `traffic`. Example: `traffic`. |
| `source` | string | yes | Regional database code (for example: us). Example: `us`. |
| `target` | string | yes | Target domain or URL (for example: seranking.com). Example: `seranking.com`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "keywordsCount": 1,
      "priceSum": 1,
      "trafficPercent": 1,
      "trafficSum": 1,
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `keywordsCount` | number | Keyword count for the subdomain. |
| `priceSum` | number | Estimated traffic value for the subdomain. |
| `trafficPercent` | number | Traffic share percentage. |
| `trafficSum` | number | Estimated traffic for the subdomain. |
| `url` | string | Subdomain URL. |

## Native endpoint

Through the native SE Ranking Data API, this operation is `GET /domain/subdomains` (base URL `https://api.seranking.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-domain-subdomains.md) for the provider-specific parameters and requirements.

