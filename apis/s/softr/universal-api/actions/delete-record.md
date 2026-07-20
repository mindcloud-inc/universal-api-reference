# Softr: Delete Record



```
DELETE https://connect.mindcloud.co/v1/universal/softr/latest/actions/delete-record
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Softr `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/softr/latest/actions/delete-record?connectionId=$CONNECTION_ID&databaseId=string&tableId=string&recordId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "databaseId": "string",
  "tableId": "string",
  "recordId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/softr/latest/actions/delete-record?${params}`, {
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
| `databaseId` | string | yes | The database ID that contains the table. |
| `tableId` | string | yes | The table ID that contains the record. |
| `recordId` | string | yes | The record ID to delete. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "recordId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `recordId` | string |  |

## Native endpoint

Through the native Softr API, this operation is `DELETE /databases/:databaseId/tables/:tableId/records/:recordId` (base URL `https://tables-api.softr.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-record.md) for the provider-specific parameters and requirements.

