# Mem: Search Collections

Finds collections in Mem by search query.

```
GET https://connect.mindcloud.co/v1/universal/mem/latest/actions/search-collections
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mem `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mem/latest/actions/search-collections?connectionId=$CONNECTION_ID&query=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "query": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mem/latest/actions/search-collections?${params}`, {
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
| `query` | string | yes | Search query text. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "requestId": "string",
      "results": [
        {
          "createdAt": "2026-05-07T12:00:00.000Z",
          "description": "string",
          "id": "string",
          "title": "string",
          "updatedAt": "2026-05-07T12:00:00.000Z"
        }
      ],
      "total": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `requestId` | string | Mem request identifier. |
| `results[].createdAt` | date | Collection creation timestamp. |
| `results[].description` | string | Collection description. |
| `results[].id` | string | Mem collection identifier. |
| `results[].title` | string | Collection title. |
| `results[].updatedAt` | date | Collection last update timestamp. |
| `total` | number | Total matching collections. |

## Native endpoint

Through the native Mem API, this operation is `POST /v2/collections/search` (base URL `https://api.mem.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-collections.md) for the provider-specific parameters and requirements.

