# Coda: Update Row

Updates a row in a Coda table.

```
PUT https://connect.mindcloud.co/v1/universal/coda/latest/actions/update-row
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Coda `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/coda/latest/actions/update-row" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "docId": "string",
  "tableIdOrName": "Ava Chen",
  "rowIdOrName": "Ava Chen",
  "row": {},
  "row.cells[]": [
    {}
  ],
  "row.cells[].column": "string",
  "row.cells[].value": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/coda/latest/actions/update-row', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "docId": "string",
    "tableIdOrName": "Ava Chen",
    "rowIdOrName": "Ava Chen",
    "row": {},
    "row.cells[]": [{}],
    "row.cells[].column": "string",
    "row.cells[].value": "string"
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
| `rowIdOrName` | list | yes |  |
| `disableParsing` | boolean | no |  |
| `row` | object | yes |  |
| `row.cells[]` | array<object> | yes |  |
| `row.cells[].column` | list | yes |  |
| `row.cells[].value` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "requestId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |
| `requestId` | string |  |

## Native endpoint

Through the native Coda API, this operation is `PUT /docs/:docId/tables/:tableIdOrName/rows/:rowIdOrName` (base URL `https://coda.io/apis/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-row.md) for the provider-specific parameters and requirements.

