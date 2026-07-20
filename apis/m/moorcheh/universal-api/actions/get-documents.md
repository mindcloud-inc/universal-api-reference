# Moorcheh: Get Documents

Retrieves specific documents from a Moorcheh namespace by ID.

```
GET https://connect.mindcloud.co/v1/universal/moorcheh/latest/actions/get-documents
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Moorcheh `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/moorcheh/latest/actions/get-documents?connectionId=$CONNECTION_ID&namespace_name=Ava%20Chen&ids%5B%5D=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "namespace_name": "Ava Chen",
  "ids[]": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/moorcheh/latest/actions/get-documents?${params}`, {
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
| `namespace_name` | string | yes | Name of the namespace containing the documents. |
| `ids[]` | array<string> | yes | Array of document IDs to retrieve. Moorcheh allows up to 100 IDs per request. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "found_items": 1,
      "items": [
        {
          "id": "string",
          "metadata": {},
          "text": "string"
        }
      ],
      "message": "string",
      "not_found_ids": [
        "string"
      ],
      "requested_ids": 1,
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `found_items` | number | Number of items found. |
| `items` | array<object> | Retrieved document objects. |
| `items[].id` | string | Document ID. |
| `items[].metadata` | object | Document metadata. |
| `items[].text` | string | Document text. |
| `message` | string | Human-readable retrieval message. |
| `not_found_ids` | array<string> | IDs not found in partial responses. |
| `requested_ids` | number | Number of requested IDs. |
| `status` | string | Retrieval status. |

## Native endpoint

Through the native Moorcheh API, this operation is `POST /namespaces/:namespace_name/documents/get` (base URL `https://api.moorcheh.ai/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-documents.md) for the provider-specific parameters and requirements.

