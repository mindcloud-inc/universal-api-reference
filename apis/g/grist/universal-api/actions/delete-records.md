# Grist: Delete Records

Deletes records from a Grist table.

```
DELETE https://connect.mindcloud.co/v1/universal/grist/latest/actions/delete-records
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Grist `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/grist/latest/actions/delete-records?connectionId=$CONNECTION_ID&docId=string&tableId=string&records%5B%5D=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "docId": "string",
  "tableId": "string",
  "records[]": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/grist/latest/actions/delete-records?${params}`, {
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
| `tableId` | string | yes | Table ID (e.g. Table1) |
| `records[]` | array<number> | yes | Array of integer record IDs to delete, e.g. [1,2,3] |

## Response

```json
{
  "success": true,
  "data": [
    {
      "value": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `value` | string | Empty response body. Grist docs for POST /docs/{docId}/tables/{tableId}/records/delete document HTTP 200 with 'Nothing returned'. |

## Native endpoint

Through the native Grist API, this operation is `POST /docs/:docId/tables/:tableId/records/delete` (base URL `https://docs.getgrist.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-records.md) for the provider-specific parameters and requirements.

