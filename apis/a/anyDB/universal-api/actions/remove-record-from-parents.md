# AnyDB: Remove Record From Parents

Removes a record from parent records in AnyDB.

```
DELETE https://connect.mindcloud.co/v1/universal/anyDB/latest/actions/remove-record-from-parents
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a AnyDB `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/anyDB/latest/actions/remove-record-from-parents?connectionId=$CONNECTION_ID&recordId=string&databaseId=string&teamId=string&removeFromIds=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "recordId": "string",
  "databaseId": "string",
  "teamId": "string",
  "removeFromIds": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/anyDB/latest/actions/remove-record-from-parents?${params}`, {
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
| `recordId` | string | yes | The AnyDB record ID. |
| `databaseId` | string | yes | The AnyDB database ID. |
| `teamId` | string | yes | The AnyDB team ID. |
| `removeFromIds` | string<string> | yes | Comma-separated AnyDB parent IDs to detach the record from. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native AnyDB API returns.

## Native endpoint

Through the native AnyDB API, this operation is `DELETE /api/integrations/ext/remove` (base URL `https://app.anydb.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/remove-record-from-parents.md) for the provider-specific parameters and requirements.

