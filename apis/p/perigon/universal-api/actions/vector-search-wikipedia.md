# Perigon: Vector Search Wikipedia

Finds Wikipedia pages by semantic similarity through Perigon.

```
GET https://connect.mindcloud.co/v1/universal/perigon/latest/actions/vector-search-wikipedia
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Perigon `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/perigon/latest/actions/vector-search-wikipedia?connectionId=$CONNECTION_ID&prompt=artificial%20intelligence%20and%20neural%20networks%20in%20computing" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "prompt": "artificial intelligence and neural networks in computing"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/perigon/latest/actions/vector-search-wikipedia?${params}`, {
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
| `prompt` | string | yes | Example: `artificial intelligence and neural networks in computing`. |
| `filter` | object | no | Example: `[object Object]`. |
| `wikiRevisionFrom` | date | no | Example: `2026-01-01T00:00:00`. |
| `wikiRevisionTo` | date | no | Example: `2026-04-09T23:59:59`. |
| `pageviewsFrom` | number | no | Example: `100`. |
| `pageviewsTo` | number | no | Example: `100000`. |
| `size` | number | no | Example: `10`. |
| `page` | number | no | Example: `0`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "results": [
        {}
      ],
      "status": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `results` | array<object> |  |
| `status` | number |  |

## Native endpoint

Through the native Perigon API, this operation is `POST /v1/vector/wikipedia/all` (base URL `https://api.perigon.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/vector-search-wikipedia.md) for the provider-specific parameters and requirements.

