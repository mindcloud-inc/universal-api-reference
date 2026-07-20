# NocoDB: Delete Table Records

Deletes records from a NocoDB table.

```
DELETE https://connect.mindcloud.co/v1/universal/nocoDB/latest/actions/delete-table-records
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a NocoDB `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/nocoDB/latest/actions/delete-table-records?connectionId=$CONNECTION_ID&baseId=string&tableId=string&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "baseId": "string",
  "tableId": "string",
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/nocoDB/latest/actions/delete-table-records?${params}`, {
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
| `id` | string | yes | Record identifier. |

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

Through the native NocoDB API, this operation is `DELETE /api/v3/data/:baseId/:tableId/records` (base URL `https://app.nocodb.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-table-records.md) for the provider-specific parameters and requirements.

