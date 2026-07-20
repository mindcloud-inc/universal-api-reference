# SE Ranking Data: List referring IPs

Retrieves referring IPs from SE Ranking Data.

```
GET https://connect.mindcloud.co/v1/universal/seRanking/latest/actions/list-referring-ips
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SE Ranking Data `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/seRanking/latest/actions/list-referring-ips?connectionId=$CONNECTION_ID&target=seranking.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "target": "seranking.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/seRanking/latest/actions/list-referring-ips?${params}`, {
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
      "ips": [
        {
          "backlinks": 1,
          "dofollowBacklinks": 1,
          "firstSeen": "string",
          "ip": "string",
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
| `ips` | array<object> | Referring IP rows. |
| `ips[].backlinks` | number |  |
| `ips[].dofollowBacklinks` | number |  |
| `ips[].firstSeen` | string |  |
| `ips[].ip` | string |  |
| `ips[].lastVisited` | string |  |
| `ips[].nofollowBacklinks` | number |  |
| `ips[].refdomains` | number |  |

## Native endpoint

Through the native SE Ranking Data API, this operation is `GET /backlinks/referring-ips` (base URL `https://api.seranking.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-referring-ips.md) for the provider-specific parameters and requirements.

