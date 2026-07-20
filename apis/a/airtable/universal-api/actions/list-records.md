# Airtable: List Records

Retrieves records from a specific Airtable table.

```
GET https://connect.mindcloud.co/v1/universal/airtable/latest/actions/list-records
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Airtable `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/airtable/latest/actions/list-records?connectionId=$CONNECTION_ID&limit=25&offset=0&baseId=string&tableId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "baseId": "string",
  "tableId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/airtable/latest/actions/list-records?${params}`, {
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
| `baseId` | list<string> | yes | To get this value, check this doc https://airtable.com/developers/web/api/list-bases |
| `filterByFormula` | string | no |  |
| `tableId` | list<string> | yes |  |
| `sort[0][field]` | string | no | Enter a Field name to sort by. |
| `sort[0][direction]` | list<string> | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdTime": "2026-05-07T12:00:00.000Z",
      "fields": {
        "attachmentSummary": {
          "errorType": "string",
          "isStale": true,
          "state": "string",
          "value": {}
        },
        "name": "Ava Chen"
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
| `fields.attachmentSummary.errorType` | string |  |
| `fields.attachmentSummary.isStale` | boolean |  |
| `fields.attachmentSummary.state` | string |  |
| `fields.attachmentSummary.value` | object |  |
| `fields.name` | string |  |
| `id` | string |  |
| `viewRecord` | string |  |

## Native endpoint

Through the native Airtable API, this operation is `GET /:baseId/:tableId` (base URL `https://api.airtable.com/v0`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-records.md) for the provider-specific parameters and requirements.

