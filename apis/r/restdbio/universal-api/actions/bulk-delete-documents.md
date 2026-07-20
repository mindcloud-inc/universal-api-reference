# Restdb.io: Bulk Delete Documents

Deletes multiple documents from Restdb.io by ID list.

```
DELETE https://connect.mindcloud.co/v1/universal/restdbio/latest/actions/bulk-delete-documents
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Restdb.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/restdbio/latest/actions/bulk-delete-documents?connectionId=$CONNECTION_ID&collection=string&ids=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "collection": "string",
  "ids": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/restdbio/latest/actions/bulk-delete-documents?${params}`, {
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
| `collection` | string | yes | Collection name in the target Restdb.io database. |
| `ids` | string | yes | Array of Restdb.io ObjectIDs to delete. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Restdb.io API returns.

## Native endpoint

Through the native Restdb.io API, this operation is `DELETE /rest/:collection/*` (base URL `https://mindcloudstage0-7934.restdb.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/bulk-delete-documents.md) for the provider-specific parameters and requirements.

