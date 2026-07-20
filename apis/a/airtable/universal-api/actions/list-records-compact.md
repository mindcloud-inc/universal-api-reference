# Airtable: List Records - Compact

Retrieves selected fields from records in a specific Airtable table.

```
GET https://connect.mindcloud.co/v1/universal/airtable/latest/actions/list-records-compact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Airtable `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/airtable/latest/actions/list-records-compact?connectionId=$CONNECTION_ID&limit=25&offset=0&baseId=string&fields=string&tableId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "baseId": "string",
  "fields": "string",
  "tableId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/airtable/latest/actions/list-records-compact?${params}`, {
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
| `baseId` | list<string> | yes |  |
| `filterByFormula` | string | no | Leave blank to return all records in this table. If the record has a blank value for one of the fields specified below, the field is omitted from the response. Wrap column names in curly brackets ({}) and use single quotes ('') to wrap string and date values. Example: {SKU} = '12345' |
| `fields` | list<string> | yes | The Field Names or Field Id to return in the response. (case-sensitive) Accepts multiple values as an array. |
| `tableId` | list<string> | yes |  |
| `offset` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdTime": "2026-05-07T12:00:00.000Z",
      "fields": {
        "manufacturer": "string",
        "sku": "string"
      },
      "id": "string",
      "viewRecord": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdTime` | date |  |
| `fields.manufacturer` | string |  |
| `fields.sku` | string |  |
| `id` | string |  |
| `viewRecord` | string |  |

## Native endpoint

Through the native Airtable API, this operation is `POST /:baseId/:tableId/listRecords` (base URL `https://api.airtable.com/v0`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-records-compact.md) for the provider-specific parameters and requirements.

