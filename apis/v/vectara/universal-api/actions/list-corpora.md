# Vectara: List Corpora

Retrieves a list of corpora from Vectara.

```
GET https://connect.mindcloud.co/v1/universal/vectara/latest/actions/list-corpora
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Vectara `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/vectara/latest/actions/list-corpora?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/vectara/latest/actions/list-corpora?${params}`, {
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
| `filter` | string | no | Filter corpora by name or summary. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `corpusId` | string<string> | no | Limit results to the specified corpus IDs. |
| `pageKey` | string | no | Return the next page of corpora. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "corpora": [
        {}
      ],
      "metadata": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `corpora` | array<object> | List of corpora. |
| `metadata` | object | Pagination metadata for the list response. |

## Native endpoint

Through the native Vectara API, this operation is `GET /v2/corpora` (base URL `https://api.vectara.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-corpora.md) for the provider-specific parameters and requirements.

