# Softr: Search Records



```
GET https://connect.mindcloud.co/v1/universal/softr/latest/actions/search-records
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Softr `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/softr/latest/actions/search-records?connectionId=$CONNECTION_ID&databaseId=string&tableId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "databaseId": "string",
  "tableId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/softr/latest/actions/search-records?${params}`, {
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
| `tableId` | string | yes | The table ID to search records in. |
| `fieldNames` | boolean | no | Return field names instead of field IDs in the response. |
| `filter` | object | no | The filter object for the search request. |
| `sorting` | list<object> | no | The sorting array for the search request. |
| `paging` | object | no | The paging object for the search request. |

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

Through the native Softr API, this operation is `POST /databases/:databaseId/tables/:tableId/records/search` (base URL `https://tables-api.softr.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-records.md) for the provider-specific parameters and requirements.

