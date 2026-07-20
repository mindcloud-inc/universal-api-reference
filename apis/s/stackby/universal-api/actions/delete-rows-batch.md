# Stackby: Delete Rows Batch

Deletes existing rows from a Stackby table.

```
DELETE https://connect.mindcloud.co/v1/universal/stackby/latest/actions/delete-rows-batch
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Stackby `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/stackby/latest/actions/delete-rows-batch?connectionId=$CONNECTION_ID&stackId=string&tableName=Ava%20Chen&rowIdsQuery=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "stackId": "string",
  "tableName": "Ava Chen",
  "rowIdsQuery": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/stackby/latest/actions/delete-rows-batch?${params}`, {
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
| `stackId` | string | yes | Stack identifier from Stackby. |
| `tableName` | string | yes | Table name from Stackby. |
| `rowIdsQuery` | string | yes | Exact query string such as rowIds[]=rw123&rowIds[]=rw456. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "records": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `records` | array<object> | Deletion result records including deleted status. |

## Native endpoint

Through the native Stackby API, this operation is `DELETE /betav1/rowdelete/{{stackId}}/{{tableName}}?{{rowIdsQuery}}` (base URL `https://stackby.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-rows-batch.md) for the provider-specific parameters and requirements.

