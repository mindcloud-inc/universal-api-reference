# SE Ranking Project: List Competitors

Retrieves project competitors from SE Ranking.

```
GET https://connect.mindcloud.co/v1/universal/sERankingProject/latest/actions/list-competitors
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SE Ranking Project `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sERankingProject/latest/actions/list-competitors?connectionId=$CONNECTION_ID&site_id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "site_id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sERankingProject/latest/actions/list-competitors?${params}`, {
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
| `site_id` | list<number> | yes | Project site identifier from SE Ranking. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "item": {
        "domainTrust": 1,
        "id": 1,
        "name": "Ava Chen",
        "url": "https://example.com"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `item` | object |  |
| `item.domainTrust` | number |  |
| `item.id` | number |  |
| `item.name` | string |  |
| `item.url` | string |  |

## Native endpoint

Through the native SE Ranking Project API, this operation is `GET /competitors/site/:site_id` (base URL `https://api4.seranking.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-competitors.md) for the provider-specific parameters and requirements.

