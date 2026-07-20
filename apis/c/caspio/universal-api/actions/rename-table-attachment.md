# Caspio: Rename Table Attachment

Updates table attachment metadata in Caspio.

```
PUT https://connect.mindcloud.co/v1/universal/caspio/latest/actions/rename-table-attachment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Caspio `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/caspio/latest/actions/rename-table-attachment" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "tableName": "Ava Chen",
  "attachmentFieldName": "Ava Chen",
  "where": "string",
  "fileName": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/caspio/latest/actions/rename-table-attachment', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "tableName": "Ava Chen",
    "attachmentFieldName": "Ava Chen",
    "where": "string",
    "fileName": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `tableName` | string | yes | Target table name. |
| `attachmentFieldName` | string | yes | Attachment field name. |
| `where` | string | yes | SQL-like WHERE clause that selects the row holding the file. |
| `response` | string | no | Optional response type. |
| `fileName` | string | yes | New file name. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "RecordsAffected": 1,
      "Result": [
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
| `RecordsAffected` | number |  |
| `Result` | array<object> |  |

## Native endpoint

Through the native Caspio API, this operation is `PUT /v3/tables/{tableName}/attachments/{attachmentFieldName}/fileInfo` (base URL `https://d2hbw900.caspio.com/integrations/rest`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/rename-table-attachment.md) for the provider-specific parameters and requirements.

