# Caspio: Upload Table Attachment

Uploads a table attachment to Caspio.

```
PUT https://connect.mindcloud.co/v1/universal/caspio/latest/actions/upload-table-attachment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Caspio `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/caspio/latest/actions/upload-table-attachment" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "tableName": "Ava Chen",
  "attachmentFieldName": "Ava Chen",
  "recordPkId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/caspio/latest/actions/upload-table-attachment', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "tableName": "Ava Chen",
    "attachmentFieldName": "Ava Chen",
    "recordPkId": "string"
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
| `recordPkId` | string | yes | Record primary key value. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Caspio API returns.

## Native endpoint

Through the native Caspio API, this operation is `PUT /v3/tables/{tableName}/attachments/{attachmentFieldName}/{recordPkId}` (base URL `https://d2hbw900.caspio.com/integrations/rest`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/upload-table-attachment.md) for the provider-specific parameters and requirements.

