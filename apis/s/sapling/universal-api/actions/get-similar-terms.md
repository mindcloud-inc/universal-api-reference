# Sapling: Get Similar Terms

Retrieves similar terms for text from Sapling.

```
GET https://connect.mindcloud.co/v1/universal/sapling/latest/actions/get-similar-terms
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sapling `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sapling/latest/actions/get-similar-terms?connectionId=$CONNECTION_ID&query=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "query": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sapling/latest/actions/get-similar-terms?${params}`, {
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
| `query` | string | yes | Term to find similar terms for. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "neighbors": [
        {}
      ],
      "synonyms": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `neighbors` | array<object> | Nearby terms with similarity metadata. |
| `synonyms` | array<string> | Synonym suggestions. |

## Native endpoint

Through the native Sapling API, this operation is `POST /api/v1/thesaurus` (base URL `https://api.sapling.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-similar-terms.md) for the provider-specific parameters and requirements.

