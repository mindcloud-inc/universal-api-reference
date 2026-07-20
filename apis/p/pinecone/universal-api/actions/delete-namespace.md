# Pinecone: Delete Namespace

Deletes a namespace from a Pinecone index.

```
DELETE https://connect.mindcloud.co/v1/universal/pinecone/latest/actions/delete-namespace
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pinecone `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/pinecone/latest/actions/delete-namespace?connectionId=$CONNECTION_ID&namespace=mc-stage3-ns-example" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "namespace": "mc-stage3-ns-example"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pinecone/latest/actions/delete-namespace?${params}`, {
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
| `namespace` | string | yes | The name of the namespace to delete. Example: `mc-stage3-ns-example`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Pinecone API returns.

## Native endpoint

Through the native Pinecone API, this operation is `DELETE {{credentials.indexHost}}/namespaces/:namespace` (base URL `https://api.pinecone.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-namespace.md) for the provider-specific parameters and requirements.

