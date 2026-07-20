# FlowiseAI: Delete Document Store Loader

Deletes a document loader and chunks from FlowiseAI.

```
DELETE https://connect.mindcloud.co/v1/universal/flowiseAI/latest/actions/delete-document-store-loader
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a FlowiseAI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/flowiseAI/latest/actions/delete-document-store-loader?connectionId=$CONNECTION_ID&loaderId=string&storeId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "loaderId": "string",
  "storeId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/flowiseAI/latest/actions/delete-document-store-loader?${params}`, {
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
| `loaderId` | string | yes | Loader ID within the document store. |
| `storeId` | string | yes | Document store ID. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native FlowiseAI API returns.

## Native endpoint

Through the native FlowiseAI API, this operation is `DELETE /document-store/loader/{storeId}/{loaderId}` (base URL `https://cloud.flowiseai.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-document-store-loader.md) for the provider-specific parameters and requirements.

