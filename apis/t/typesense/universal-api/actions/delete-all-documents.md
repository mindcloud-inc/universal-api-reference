# Typesense: Delete All Documents

Deletes all documents from a Typesense collection.

```
DELETE https://connect.mindcloud.co/v1/universal/typesense/latest/actions/delete-all-documents
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Typesense `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/typesense/latest/actions/delete-all-documents?connectionId=$CONNECTION_ID&collection=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "collection": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/typesense/latest/actions/delete-all-documents?${params}`, {
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
| `collection` | string | yes | Collection name. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "num_deleted": 1,
      "response": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `num_deleted` | number |  |
| `response` | object |  |

## Native endpoint

Through the native Typesense API, this operation is `DELETE /collections/{{collection}}/documents` (base URL `https://5brh8vz1lictf0jop-1.a2.typesense.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-all-documents.md) for the provider-specific parameters and requirements.

