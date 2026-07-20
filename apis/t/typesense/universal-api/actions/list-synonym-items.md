# Typesense: List Synonym Items

Retrieves synonyms from a Typesense synonym set.

```
GET https://connect.mindcloud.co/v1/universal/typesense/latest/actions/list-synonym-items
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Typesense `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/typesense/latest/actions/list-synonym-items?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/typesense/latest/actions/list-synonym-items?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "response": {},
      "synonyms": [
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
| `response` | object |  |
| `synonyms` | array<object> |  |

## Native endpoint

Through the native Typesense API, this operation is `GET /synonym_sets/{{synonymSetName}}/items` (base URL `https://5brh8vz1lictf0jop-1.a2.typesense.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-synonym-items.md) for the provider-specific parameters and requirements.

