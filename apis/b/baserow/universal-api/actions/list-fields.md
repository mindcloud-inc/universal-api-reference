# Baserow: List Fields

Retrieves fields from a Baserow table.

```
GET https://connect.mindcloud.co/v1/universal/baserow/latest/actions/list-fields
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Baserow `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/baserow/latest/actions/list-fields?connectionId=$CONNECTION_ID&tableId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "tableId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/baserow/latest/actions/list-fields?${params}`, {
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
| `tableId` | number | yes | The Baserow table whose fields you want to inspect. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "databaseId": 1,
      "dbIndex": true,
      "description": {},
      "id": 1,
      "immutableProperties": true,
      "immutableType": true,
      "longTextEnableRichText": true,
      "name": "Ava Chen",
      "order": 1,
      "primary": true,
      "readOnly": true,
      "tableId": 1,
      "textDefault": "string",
      "type": "string",
      "workspaceId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `databaseId` | number |  |
| `dbIndex` | boolean |  |
| `description` | object |  |
| `id` | number |  |
| `immutableProperties` | boolean |  |
| `immutableType` | boolean |  |
| `longTextEnableRichText` | boolean |  |
| `name` | string |  |
| `order` | number |  |
| `primary` | boolean |  |
| `readOnly` | boolean |  |
| `tableId` | number |  |
| `textDefault` | string |  |
| `type` | string |  |
| `workspaceId` | number |  |

## Native endpoint

Through the native Baserow API, this operation is `GET /api/database/fields/table/:table_id/` (base URL `https://api.baserow.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-fields.md) for the provider-specific parameters and requirements.

