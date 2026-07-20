# Grist: List Tables

Finds tables in a Grist document.

```
GET https://connect.mindcloud.co/v1/universal/grist/latest/actions/list-tables
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Grist `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/grist/latest/actions/list-tables?connectionId=$CONNECTION_ID&docId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "docId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/grist/latest/actions/list-tables?${params}`, {
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

## Response

```json
{
  "success": true,
  "data": [
    {
      "tables": [
        {
          "fields": {
            "onDemand": true,
            "primaryViewId": 1,
            "rawViewSectionRef": 1,
            "recordCardViewSectionRef": 1,
            "summarySourceTable": 1,
            "tableRef": 1
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
| `tables[].fields.onDemand` | boolean |  |
| `tables[].fields.primaryViewId` | number |  |
| `tables[].fields.rawViewSectionRef` | number |  |
| `tables[].fields.recordCardViewSectionRef` | number |  |
| `tables[].fields.summarySourceTable` | number |  |
| `tables[].fields.tableRef` | number |  |
| `tables[].id` | string |  |

## Native endpoint

Through the native Grist API, this operation is `GET /docs/:docId/tables` (base URL `https://docs.getgrist.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-tables.md) for the provider-specific parameters and requirements.

