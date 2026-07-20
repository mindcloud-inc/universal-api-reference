# Grist: Replace Records

Replaces records in a Grist table.

```
PUT https://connect.mindcloud.co/v1/universal/grist/latest/actions/replace-records
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Grist `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/grist/latest/actions/replace-records" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "docId": "string",
  "tableId": "string",
  "records": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/grist/latest/actions/replace-records', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "docId": "string",
    "tableId": "string",
    "records": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `docId` | string | yes | Document ID |
| `tableId` | list<string> | yes | Table ID (e.g. Table1) |
| `records` | string | yes | Array of {require: {col: val}, fields: {col: val}} |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `noparse` | boolean | no | Skip string parsing |
| `onmany` | string | no | When multiple match: first, none, or all |
| `noadd` | boolean | no | Do not add new records |
| `noupdate` | boolean | no | Do not update existing records |

## Response

```json
{
  "success": true,
  "data": [
    {
      "value": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `value` | string | Empty response body. Grist docs for PUT /docs/{docId}/tables/{tableId}/records document HTTP 200 with 'Nothing returned'. |

## Native endpoint

Through the native Grist API, this operation is `PUT /docs/:docId/tables/:tableId/records` (base URL `https://docs.getgrist.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/replace-records.md) for the provider-specific parameters and requirements.

