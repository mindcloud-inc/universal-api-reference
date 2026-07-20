# Perigon: Vector Search Articles

Finds Perigon articles by semantic similarity to a prompt.

```
GET https://connect.mindcloud.co/v1/universal/perigon/latest/actions/vector-search-articles
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Perigon `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/perigon/latest/actions/vector-search-articles?connectionId=$CONNECTION_ID&prompt=Latest%20advancements%20in%20artificial%20intelligence" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "prompt": "Latest advancements in artificial intelligence"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/perigon/latest/actions/vector-search-articles?${params}`, {
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
| `prompt` | string | yes | Example: `Latest advancements in artificial intelligence`. |
| `filter` | object | no | Example: `[object Object]`. |
| `pubDateFrom` | date | no | Example: `2026-03-10T00:00:00`. |
| `pubDateTo` | date | no | Example: `2026-04-09T23:59:59`. |
| `showReprints` | boolean | no |  |
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

Through the native Perigon API, this operation is `POST /v1/vector/news/all` (base URL `https://api.perigon.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/vector-search-articles.md) for the provider-specific parameters and requirements.

