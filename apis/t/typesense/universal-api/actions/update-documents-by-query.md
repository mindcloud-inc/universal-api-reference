# Typesense: Update Documents By Query

Updates matching documents in a Typesense collection.

```
PUT https://connect.mindcloud.co/v1/universal/typesense/latest/actions/update-documents-by-query
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Typesense `connectionId` ([setup](../authentication.md)).

This action also supports [filtering](../filtering.md) (`where`).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/typesense/latest/actions/update-documents-by-query" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "collection": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/typesense/latest/actions/update-documents-by-query', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "collection": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `collection` | string | yes | Collection name. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "num_updated": 1,
      "response": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `num_updated` | number |  |
| `response` | object |  |

## Native endpoint

Through the native Typesense API, this operation is `PATCH /collections/{{collection}}/documents` (base URL `https://5brh8vz1lictf0jop-1.a2.typesense.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-documents-by-query.md) for the provider-specific parameters and requirements.

