# KIS: Delete Record

Deletes an existing record from a KIS data table.

```
DELETE https://connect.mindcloud.co/v1/universal/kIS/latest/actions/delete-record
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a KIS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/kIS/latest/actions/delete-record?connectionId=$CONNECTION_ID&recordId=string&collectionName=Ava%20Chen&documentId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "recordId": "string",
  "collectionName": "Ava Chen",
  "documentId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/kIS/latest/actions/delete-record?${params}`, {
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
| `recordId` | string | yes | KIS object ID for the record to delete. Used in the request path. |
| `collectionName` | string | yes | Exact KIS table name containing the record. |
| `documentId` | string | yes | KIS object ID for the record to delete. Must match the path record ID. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native KIS API returns.

## Native endpoint

Through the native KIS API, this operation is `DELETE /api_token_access/data_handlers/{recordId}` (base URL `https://api.getkis.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-record.md) for the provider-specific parameters and requirements.

