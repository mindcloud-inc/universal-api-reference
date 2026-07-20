# Weaviate Vector Store: Get an object

Retrieves an object from Weaviate.

```
GET https://connect.mindcloud.co/v1/universal/weaviateVectorStore/latest/actions/objects-class-get
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Weaviate Vector Store `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/weaviateVectorStore/latest/actions/objects-class-get?connectionId=$CONNECTION_ID&classname=Ava%20Chen&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "classname": "Ava Chen",
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/weaviateVectorStore/latest/actions/objects-class-get?${params}`, {
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
| `classname` | string | yes | Name of the collection (class) the object belongs to. |
| `id` | string | yes | Unique UUID of the object to be retrieved. |
| `include` | string | no | Include additional information, such as classification information. Allowed values include: `classification`, `vector` and `interpretation`. |
| `consistencyLevel` | string | no | Determines how many replicas must acknowledge a request before it is considered successful. |
| `nodeName` | string | no | The target node which should fulfill the request. |
| `tenant` | string | no | Specifies the tenant in a request targeting a multi-tenant collection (class). |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Weaviate Vector Store API returns.

## Native endpoint

Through the native Weaviate Vector Store API, this operation is `GET /objects/:className/:id` (base URL `https://tl3apaxxsoiuwhpnsdv19a.c0.us-west3.gcp.weaviate.cloud`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/objects-class-get.md) for the provider-specific parameters and requirements.

