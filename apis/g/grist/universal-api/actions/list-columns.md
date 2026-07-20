# Grist: List Columns

Finds columns in a Grist table.

```
GET https://connect.mindcloud.co/v1/universal/grist/latest/actions/list-columns
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Grist `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/grist/latest/actions/list-columns?connectionId=$CONNECTION_ID&docId=string&tableId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "docId": "string",
  "tableId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/grist/latest/actions/list-columns?${params}`, {
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
| `docId` | string | yes | Document ID |
| `tableId` | list<string> | yes | Table ID (e.g. Table1) |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `hidden` | boolean | no | Include hidden columns |

## Response

```json
{
  "success": true,
  "data": [
    {
      "columns": [
        {
          "fields": {
            "colRef": 1,
            "description": "string",
            "displayCol": 1,
            "formula": "string",
            "isFormula": true,
            "label": "string",
            "parentId": 1,
            "parentPos": 1,
            "recalcDeps": {},
            "recalcWhen": 1,
            "reverseCol": 1,
            "rules": {},
            "summarySourceCol": 1,
            "type": "string",
            "untieColIdFromLabel": true,
            "visibleCol": 1,
            "widgetOptions": "string"
          },
          "id": "string"
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
| `columns[].fields.colRef` | number |  |
| `columns[].fields.description` | string |  |
| `columns[].fields.displayCol` | number |  |
| `columns[].fields.formula` | string |  |
| `columns[].fields.isFormula` | boolean |  |
| `columns[].fields.label` | string |  |
| `columns[].fields.parentId` | number |  |
| `columns[].fields.parentPos` | number |  |
| `columns[].fields.recalcDeps` | object |  |
| `columns[].fields.recalcWhen` | number |  |
| `columns[].fields.reverseCol` | number |  |
| `columns[].fields.rules` | object |  |
| `columns[].fields.summarySourceCol` | number |  |
| `columns[].fields.type` | string |  |
| `columns[].fields.untieColIdFromLabel` | boolean |  |
| `columns[].fields.visibleCol` | number |  |
| `columns[].fields.widgetOptions` | string |  |
| `columns[].id` | string |  |

## Native endpoint

Through the native Grist API, this operation is `GET /docs/:docId/tables/:tableId/columns` (base URL `https://docs.getgrist.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-columns.md) for the provider-specific parameters and requirements.

