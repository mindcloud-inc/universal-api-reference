# Vectara: List Rerankers

Retrieves the available rerankers from Vectara.

```
GET https://connect.mindcloud.co/v1/universal/vectara/latest/actions/list-rerankers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Vectara `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/vectara/latest/actions/list-rerankers?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/vectara/latest/actions/list-rerankers?${params}`, {
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
| `filter` | string | no | Regex filter against reranker names and descriptions. |
| `limit` | number | no | Maximum number of rerankers to return. |
| `pageKey` | string | no | Cursor for the next page of rerankers. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "metadata": {},
      "rerankers": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `metadata` | object | Pagination metadata for the list response. |
| `rerankers` | array<object> | List of rerankers. |

## Native endpoint

Through the native Vectara API, this operation is `GET /v2/rerankers` (base URL `https://api.vectara.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-rerankers.md) for the provider-specific parameters and requirements.

