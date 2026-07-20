# Softr: Create Record



```
POST https://connect.mindcloud.co/v1/universal/softr/latest/actions/create-record
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Softr `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/softr/latest/actions/create-record" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "databaseId": "string",
  "tableId": "string",
  "fields": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/softr/latest/actions/create-record', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "databaseId": "string",
    "tableId": "string",
    "fields": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `databaseId` | string | yes | The database ID that contains the table. |
| `tableId` | string | yes | The table ID to create the record in. |
| `fieldNames` | boolean | no | Return field names instead of field IDs in the response. |
| `fields` | object | yes | The field values to create on the record. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "2026-05-07T12:00:00.000Z",
      "fields": {},
      "id": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date | When the record was created. |
| `fields` | object | The record field values keyed by field name or field ID. |
| `id` | string | The record ID. |
| `updatedAt` | date | When the record was last updated. |

## Native endpoint

Through the native Softr API, this operation is `POST /databases/:databaseId/tables/:tableId/records` (base URL `https://tables-api.softr.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-record.md) for the provider-specific parameters and requirements.

