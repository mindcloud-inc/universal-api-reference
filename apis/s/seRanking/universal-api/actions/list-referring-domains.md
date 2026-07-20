# SE Ranking Data: List referring domains

Retrieves referring domains from SE Ranking Data.

```
GET https://connect.mindcloud.co/v1/universal/seRanking/latest/actions/list-referring-domains
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SE Ranking Data `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/seRanking/latest/actions/list-referring-domains?connectionId=$CONNECTION_ID&target=seranking.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "target": "seranking.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/seRanking/latest/actions/list-referring-domains?${params}`, {
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
      "refdomains": [
        {
          "backlinks": 1,
          "dofollowBacklinks": 1,
          "domainInlinkRank": 1,
          "firstSeen": "string",
          "refdomain": "string"
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
| `refdomains` | array<object> | Referring domain rows. |
| `refdomains[].backlinks` | number |  |
| `refdomains[].dofollowBacklinks` | number |  |
| `refdomains[].domainInlinkRank` | number |  |
| `refdomains[].firstSeen` | string |  |
| `refdomains[].refdomain` | string |  |

## Native endpoint

Through the native SE Ranking Data API, this operation is `GET /backlinks/refdomains` (base URL `https://api.seranking.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-referring-domains.md) for the provider-specific parameters and requirements.

