# Moorcheh: Create Namespace

Creates a new namespace in Moorcheh.

```
POST https://connect.mindcloud.co/v1/universal/moorcheh/latest/actions/create-namespace
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Moorcheh `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/moorcheh/latest/actions/create-namespace" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "namespace_name": "Ava Chen",
  "type": "text"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/moorcheh/latest/actions/create-namespace', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "namespace_name": "Ava Chen",
    "type": "text"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `namespace_name` | string | yes | Unique namespace name using only alphanumeric characters, hyphens, and underscores. |
| `type` | string | yes | Namespace type: text for documents or vector for pre-computed embeddings. Example: `text`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `vector_dimension` | number | no | Required for vector namespaces. Dimension of vectors to be stored, such as 1536. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string",
      "namespace_name": "Ava Chen",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string | Human-readable creation message. |
| `namespace_name` | string | Created namespace name. |
| `status` | string | Creation status. |

## Native endpoint

Through the native Moorcheh API, this operation is `POST /namespaces` (base URL `https://api.moorcheh.ai/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-namespace.md) for the provider-specific parameters and requirements.

