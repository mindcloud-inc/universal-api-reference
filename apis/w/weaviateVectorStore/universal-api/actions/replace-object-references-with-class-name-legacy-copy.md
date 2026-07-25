# Weaviate Vector Store: Replace Object References with Class Name (Legacy Copy)

Replaces object references in Weaviate.

```
PUT https://connect.mindcloud.co/v1/universal/weaviateVectorStore/latest/actions/replace-object-references-with-class-name-legacy-copy
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Weaviate Vector Store `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/weaviateVectorStore/latest/actions/replace-object-references-with-class-name-legacy-copy" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "classname": "Ava Chen",
  "id": "string",
  "propertyname": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/weaviateVectorStore/latest/actions/replace-object-references-with-class-name-legacy-copy', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "classname": "Ava Chen",
    "id": "string",
    "propertyname": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `classname` | string | yes | Name of the collection (class) the source object belongs to. |
| `id` | string | yes | Unique UUID of the source object. |
| `propertyname` | string | yes | Unique name of the reference property of the source object. |
| `consistencyLevel` | string | no | Determines how many replicas must acknowledge a request before it is considered successful. |
| `tenant` | string | no | Specifies the tenant in a request targeting a multi-tenant collection (class). |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Weaviate Vector Store API returns.

## Native endpoint

Through the native Weaviate Vector Store API, this operation is `PUT /objects/:className/:id/references/:propertyName` (base URL `https://tl3apaxxsoiuwhpnsdv19a.c0.us-west3.gcp.weaviate.cloud`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/replace-object-references-with-class-name-legacy-copy.md) for the provider-specific parameters and requirements.

