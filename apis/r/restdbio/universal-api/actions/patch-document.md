# Restdb.io: Patch Document

Updates selected fields on a Restdb.io document.

```
PUT https://connect.mindcloud.co/v1/universal/restdbio/latest/actions/patch-document
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Restdb.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/restdbio/latest/actions/patch-document" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "collection": "string",
  "documentId": "string",
  "patch": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/restdbio/latest/actions/patch-document', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "collection": "string",
    "documentId": "string",
    "patch": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `collection` | string | yes | Collection name in the target Restdb.io database. |
| `documentId` | string | yes | Restdb.io ObjectID of the document. |
| `patch` | string | yes | JSON object with the properties to update. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Restdb.io API returns.

## Native endpoint

Through the native Restdb.io API, this operation is `PATCH /rest/:collection/:documentId` (base URL `https://mindcloudstage0-7934.restdb.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/patch-document.md) for the provider-specific parameters and requirements.

