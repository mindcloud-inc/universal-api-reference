# Coda: Upsert Rows

Inserts or updates rows in a Coda table.

```
POST https://connect.mindcloud.co/v1/universal/coda/latest/actions/upsert-rows
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Coda `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/coda/latest/actions/upsert-rows" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "docId": "string",
  "tableIdOrName": "Ava Chen",
  "rows[]": [
    {}
  ],
  "rows[].cells[]": [
    {}
  ],
  "rows[].cells[].column": "string",
  "rows[].cells[].value": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/coda/latest/actions/upsert-rows', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "docId": "string",
    "tableIdOrName": "Ava Chen",
    "rows[]": [{}],
    "rows[].cells[]": [{}],
    "rows[].cells[].column": "string",
    "rows[].cells[].value": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `docId` | list | yes |  |
| `tableIdOrName` | list | yes |  |
| `disableParsing` | boolean | no |  |
| `rows[]` | array<object> | yes |  |
| `keyColumns[]` | array<string> | no |  |
| `rows[].cells[]` | array<object> | yes |  |
| `rows[].cells[].column` | list | yes |  |
| `rows[].cells[].value` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "addedRowIds": [
        "string"
      ],
      "requestId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `addedRowIds` | array<string> |  |
| `requestId` | string |  |

## Native endpoint

Through the native Coda API, this operation is `POST /docs/:docId/tables/:tableIdOrName/rows` (base URL `https://coda.io/apis/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/upsert-rows.md) for the provider-specific parameters and requirements.

