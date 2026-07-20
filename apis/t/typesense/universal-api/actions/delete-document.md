# Typesense: Delete Document

Deletes a specific document from Typesense.

```
DELETE https://connect.mindcloud.co/v1/universal/typesense/latest/actions/delete-document
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Typesense `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/typesense/latest/actions/delete-document?connectionId=$CONNECTION_ID&collection=string&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "collection": "string",
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/typesense/latest/actions/delete-document?${params}`, {
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
| `id` | string | yes | Document ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "response": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |
| `response` | object |  |

## Native endpoint

Through the native Typesense API, this operation is `DELETE /collections/{{collection}}/documents/{{id}}` (base URL `https://5brh8vz1lictf0jop-1.a2.typesense.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-document.md) for the provider-specific parameters and requirements.

