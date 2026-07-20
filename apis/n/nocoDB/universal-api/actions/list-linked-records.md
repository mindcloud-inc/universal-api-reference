# NocoDB: List Linked Records

Retrieves linked records from a NocoDB link field.

```
GET https://connect.mindcloud.co/v1/universal/nocoDB/latest/actions/list-linked-records
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a NocoDB `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/nocoDB/latest/actions/list-linked-records?connectionId=$CONNECTION_ID&limit=25&offset=0&baseId=string&tableId=string&linkFieldId=https%3A%2F%2Fexample.com&recordId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "baseId": "string",
  "tableId": "string",
  "linkFieldId": "https://example.com",
  "recordId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/nocoDB/latest/actions/list-linked-records?${params}`, {
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
| `baseId` | string | yes | Base identifier. |
| `tableId` | string | yes | Table identifier. |
| `linkFieldId` | string | yes | Link-to-another-record field identifier. |
| `recordId` | string | yes | Record identifier. |
| `fields` | string | no | Comma-separated linked-record fields to include. |
| `where` | string | no | Filter expression in NocoDB where syntax. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "records": [
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
| `records` | array<object> |  |

## Native endpoint

Through the native NocoDB API, this operation is `GET /api/v3/data/:baseId/:tableId/links/:linkFieldId/:recordId` (base URL `https://app.nocodb.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-linked-records.md) for the provider-specific parameters and requirements.

