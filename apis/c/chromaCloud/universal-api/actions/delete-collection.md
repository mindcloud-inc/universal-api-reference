# Chroma Cloud: Delete collection

Deletes a collection from Chroma Cloud.

```
DELETE https://connect.mindcloud.co/v1/universal/chromaCloud/latest/actions/delete-collection
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Chroma Cloud `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/chromaCloud/latest/actions/delete-collection?connectionId=$CONNECTION_ID&collectionId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "collectionId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/chromaCloud/latest/actions/delete-collection?${params}`, {
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
| `collectionId` | string | yes | Collection UUID. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Chroma Cloud API returns.

## Native endpoint

Through the native Chroma Cloud API, this operation is `DELETE /api/v2/tenants/:tenant/databases/:database/collections/:collection_id` (base URL `https://api.trychroma.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-collection.md) for the provider-specific parameters and requirements.

