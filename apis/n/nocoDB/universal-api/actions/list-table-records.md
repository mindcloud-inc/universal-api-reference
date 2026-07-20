# NocoDB: List Table Records

Retrieves records from a NocoDB table.

```
GET https://connect.mindcloud.co/v1/universal/nocoDB/latest/actions/list-table-records
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a NocoDB `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/nocoDB/latest/actions/list-table-records?connectionId=$CONNECTION_ID&limit=25&offset=0&baseId=string&tableId=string" \
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

const response = await fetch(`https://connect.mindcloud.co/v1/universal/nocoDB/latest/actions/list-table-records?${params}`, {
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
| `baseId` | string | yes | Base ID for the NocoDB base. |
| `tableId` | string | yes | Table ID for the NocoDB table. |
| `fields` | string | no | Comma-separated field names to include from linked records. |
| `viewId` | string | no | Only return records visible in the specified view. |
| `linksAsLtar` | boolean | no | Return linked record data instead of counts for link fields. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "fields": {},
      "id": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `fields` | object |  |
| `id` | number |  |

## Native endpoint

Through the native NocoDB API, this operation is `GET /api/v3/data/:baseId/:tableId/records` (base URL `https://app.nocodb.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-table-records.md) for the provider-specific parameters and requirements.

