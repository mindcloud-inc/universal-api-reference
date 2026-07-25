# Weaviate Vector Store: Delete a property's inverted index

Deletes a property's inverted index from Weaviate.

```
DELETE https://connect.mindcloud.co/v1/universal/weaviateVectorStore/latest/actions/delete-a-propertys-inverted-index
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Weaviate Vector Store `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/weaviateVectorStore/latest/actions/delete-a-propertys-inverted-index?connectionId=$CONNECTION_ID&classname=Ava%20Chen&propertyname=Ava%20Chen&indexname=Ava%20Chen" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "classname": "Ava Chen",
  "propertyname": "Ava Chen",
  "indexname": "Ava Chen"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/weaviateVectorStore/latest/actions/delete-a-propertys-inverted-index?${params}`, {
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
| `classname` | string | yes | The name of the collection (class) containing the property. |
| `propertyname` | string | yes | The name of the property whose inverted index should be deleted. |
| `indexname` | string | yes | The name of the inverted index to delete from the property. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Weaviate Vector Store API returns.

## Native endpoint

Through the native Weaviate Vector Store API, this operation is `DELETE /schema/:className/properties/:propertyName/index/:indexName` (base URL `https://tl3apaxxsoiuwhpnsdv19a.c0.us-west3.gcp.weaviate.cloud`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-a-propertys-inverted-index.md) for the provider-specific parameters and requirements.

