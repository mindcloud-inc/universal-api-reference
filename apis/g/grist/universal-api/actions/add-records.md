# Grist: Add Records

Creates new records in a Grist table.

```
POST https://connect.mindcloud.co/v1/universal/grist/latest/actions/add-records
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Grist `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/grist/latest/actions/add-records" \
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
const response = await fetch('https://connect.mindcloud.co/v1/universal/grist/latest/actions/add-records', {
  method: 'POST',
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
| `records` | list<string> | yes | Array of {fields: {col: val}} |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `noparse` | boolean | no | Skip string parsing |

## Response

```json
{
  "success": true,
  "data": [
    {
      "records": [
        {
          "id": 1
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `records[].id` | number |  |

## Native endpoint

Through the native Grist API, this operation is `POST /docs/:docId/tables/:tableId/records` (base URL `https://docs.getgrist.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-records.md) for the provider-specific parameters and requirements.

