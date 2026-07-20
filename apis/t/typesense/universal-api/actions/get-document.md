# Typesense: Get Document

Retrieves a specific document from Typesense.

```
GET https://connect.mindcloud.co/v1/universal/typesense/latest/actions/get-document
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Typesense `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/typesense/latest/actions/get-document?connectionId=$CONNECTION_ID&collection=string&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "collection": "string",
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/typesense/latest/actions/get-document?${params}`, {
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

Through the native Typesense API, this operation is `GET /collections/{{collection}}/documents/{{id}}` (base URL `https://5brh8vz1lictf0jop-1.a2.typesense.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-document.md) for the provider-specific parameters and requirements.

