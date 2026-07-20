# Revel Digital: Delete Data Table Row



```
DELETE https://connect.mindcloud.co/v1/universal/revelDigital/latest/actions/delete-data-table-row
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Revel Digital `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/revelDigital/latest/actions/delete-data-table-row?connectionId=$CONNECTION_ID&rowId=string&tableId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "rowId": "string",
  "tableId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/revelDigital/latest/actions/delete-data-table-row?${params}`, {
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
| `rowId` | string | yes | Unique identifier of the data table row. |
| `tableId` | string | yes | Unique identifier of the data table. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": "string",
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | string | Empty response body returned by the provider for successful no-content deletes. |
| `success` | boolean | True when the delete request completes successfully. |

## Native endpoint

Through the native Revel Digital API, this operation is `DELETE /datatables/:tableId/rows/:rowId` (base URL `https://api.reveldigital.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-data-table-row.md) for the provider-specific parameters and requirements.

