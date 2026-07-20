# SE Ranking Project: Add Competitor

Creates a tracked competitor in SE Ranking.

```
POST https://connect.mindcloud.co/v1/universal/sERankingProject/latest/actions/add-competitor
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SE Ranking Project `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/sERankingProject/latest/actions/add-competitor" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "site_id": 1,
  "url": "https://example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/sERankingProject/latest/actions/add-competitor', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "site_id": 1,
    "url": "https://example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `site_id` | list<number> | yes | Project site ID. |
| `url` | string | yes | Competitor website URL. |
| `name` | string | no | Competitor website name. |
| `subdomain_match` | number | no | Include subdomains flag (1 or 0). |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | number |  |

## Native endpoint

Through the native SE Ranking Project API, this operation is `POST /competitors` (base URL `https://api4.seranking.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-competitor.md) for the provider-specific parameters and requirements.

