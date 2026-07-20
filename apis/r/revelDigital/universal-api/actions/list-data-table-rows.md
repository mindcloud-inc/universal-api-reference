# Revel Digital: List Data Table Rows



```
GET https://connect.mindcloud.co/v1/universal/revelDigital/latest/actions/list-data-table-rows
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Revel Digital `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/revelDigital/latest/actions/list-data-table-rows?connectionId=$CONNECTION_ID&tableId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "tableId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/revelDigital/latest/actions/list-data-table-rows?${params}`, {
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
| `tableId` | string | yes | Unique identifier of the data table. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "continuationToken": "string",
      "data": [
        {}
      ],
      "totalCount": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `continuationToken` | string |  |
| `data` | array<object> |  |
| `totalCount` | number |  |

## Native endpoint

Through the native Revel Digital API, this operation is `GET /datatables/:tableId/rows` (base URL `https://api.reveldigital.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-data-table-rows.md) for the provider-specific parameters and requirements.

