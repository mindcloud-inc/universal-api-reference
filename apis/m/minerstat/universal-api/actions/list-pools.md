# Minerstat: List Pools

Retrieves mining pools from the Minerstat catalog.

```
GET https://connect.mindcloud.co/v1/universal/minerstat/latest/actions/list-pools
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Minerstat `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/minerstat/latest/actions/list-pools?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/minerstat/latest/actions/list-pools?${params}`, {
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
| `coin` | string | no | Payout coin symbol like ETH. Example: `ETH`. |
| `type` | string | no | Pool category like multipool. Example: `multipool`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "coins": {},
      "description": "string",
      "founded": 1,
      "id": "string",
      "name": "Ava Chen",
      "type": "string",
      "url": "https://example.com",
      "website": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `coins` | object |  |
| `description` | string |  |
| `founded` | number |  |
| `id` | string |  |
| `name` | string |  |
| `type` | string |  |
| `url` | string |  |
| `website` | string |  |

## Native endpoint

Through the native Minerstat API, this operation is `GET /v2/pools` (base URL `https://api.minerstat.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-pools.md) for the provider-specific parameters and requirements.

