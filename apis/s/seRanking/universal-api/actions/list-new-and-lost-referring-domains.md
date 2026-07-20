# SE Ranking Data: List new and lost referring domains

Retrieves new and lost referring domains from SE Ranking Data.

```
GET https://connect.mindcloud.co/v1/universal/seRanking/latest/actions/list-new-and-lost-referring-domains
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SE Ranking Data `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/seRanking/latest/actions/list-new-and-lost-referring-domains?connectionId=$CONNECTION_ID&target=seranking.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "target": "seranking.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/seRanking/latest/actions/list-new-and-lost-referring-domains?${params}`, {
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
      "newLostRefdomains": [
        {
          "backlinks": 1,
          "dofollowBacklinks": 1,
          "domainInlinkRank": 1,
          "firstSeen": "string",
          "newLostDate": "string",
          "newLostType": "string",
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
| `newLostRefdomains` | array<object> | New/lost referring domain rows. |
| `newLostRefdomains[].backlinks` | number |  |
| `newLostRefdomains[].dofollowBacklinks` | number |  |
| `newLostRefdomains[].domainInlinkRank` | number |  |
| `newLostRefdomains[].firstSeen` | string |  |
| `newLostRefdomains[].newLostDate` | string |  |
| `newLostRefdomains[].newLostType` | string |  |
| `newLostRefdomains[].refdomain` | string |  |

## Native endpoint

Through the native SE Ranking Data API, this operation is `GET /backlinks/refdomains/history` (base URL `https://api.seranking.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-new-and-lost-referring-domains.md) for the provider-specific parameters and requirements.

