# NocoDB: Unlink Records

Unlinks records from a NocoDB link field.

```
DELETE https://connect.mindcloud.co/v1/universal/nocoDB/latest/actions/unlink-records
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a NocoDB `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/nocoDB/latest/actions/unlink-records?connectionId=$CONNECTION_ID&baseId=string&tableId=string&linkFieldId=https%3A%2F%2Fexample.com&recordId=string&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "baseId": "string",
  "tableId": "string",
  "linkFieldId": "https://example.com",
  "recordId": "string",
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/nocoDB/latest/actions/unlink-records?${params}`, {
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
| `id` | string | yes | Adjacent record identifier to unlink. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `success` | boolean |  |

## Native endpoint

Through the native NocoDB API, this operation is `DELETE /api/v3/data/:baseId/:tableId/links/:linkFieldId/:recordId` (base URL `https://app.nocodb.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/unlink-records.md) for the provider-specific parameters and requirements.

