# Zoho Tables: List Tables

Retrieves all tables from Zoho Tables.

```
GET https://connect.mindcloud.co/v1/universal/zohoTables/latest/actions/list-tables
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Tables `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zohoTables/latest/actions/list-tables?connectionId=$CONNECTION_ID&baseId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "baseId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zohoTables/latest/actions/list-tables?${params}`, {
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
| `baseId` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "fieldsCount": 1,
      "isActiveTable": true,
      "name": "Ava Chen",
      "recordsCount": 1,
      "tableId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `fieldsCount` | number | Number of fields in the table. |
| `isActiveTable` | boolean | Whether this is the active table. |
| `name` | string | Table name. |
| `recordsCount` | number | Number of records in the table. |
| `tableId` | string | Zoho table identifier. |

## Native endpoint

Through the native Zoho Tables API, this operation is `GET /tables` (base URL `https://tables.zoho.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-tables.md) for the provider-specific parameters and requirements.

