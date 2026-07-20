# Restdb.io: Create Child Document

Creates a child document in Restdb.io.

```
POST https://connect.mindcloud.co/v1/universal/restdbio/latest/actions/create-child-document
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Restdb.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/restdbio/latest/actions/create-child-document" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "childField": "string",
  "collection": "string",
  "document": "string",
  "documentId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/restdbio/latest/actions/create-child-document', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "childField": "string",
    "collection": "string",
    "document": "string",
    "documentId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `childField` | string | yes | Child field name on the parent document. |
| `collection` | string | yes | Collection name in the target Restdb.io database. |
| `document` | string | yes | JSON child document to create. |
| `documentId` | string | yes | Restdb.io ObjectID of the parent document. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Restdb.io API returns.

## Native endpoint

Through the native Restdb.io API, this operation is `POST /rest/:collection/:documentId/:childField` (base URL `https://mindcloudstage0-7934.restdb.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-child-document.md) for the provider-specific parameters and requirements.

