# Restdb.io: Get Child Documents

Retrieves child documents from a Restdb.io record.

```
GET https://connect.mindcloud.co/v1/universal/restdbio/latest/actions/get-child-documents
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Restdb.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/restdbio/latest/actions/get-child-documents?connectionId=$CONNECTION_ID&childField=string&collection=string&documentId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "childField": "string",
  "collection": "string",
  "documentId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/restdbio/latest/actions/get-child-documents?${params}`, {
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
| `childField` | string | yes | Child field name on the parent document. |
| `collection` | string | yes | Collection name in the target Restdb.io database. |
| `documentId` | string | yes | Restdb.io ObjectID of the parent document. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Restdb.io API returns.

## Native endpoint

Through the native Restdb.io API, this operation is `GET /rest/:collection/:documentId/:childField` (base URL `https://mindcloudstage0-7934.restdb.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-child-documents.md) for the provider-specific parameters and requirements.

