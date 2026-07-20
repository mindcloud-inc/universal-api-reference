# Lasso X: List Reporting Batch Items

Retrieves items for a reporting batch from Lasso X.

```
GET https://connect.mindcloud.co/v1/universal/lassoX/latest/actions/list-reporting-batch-items
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Lasso X `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/lassoX/latest/actions/list-reporting-batch-items?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/lassoX/latest/actions/list-reporting-batch-items?${params}`, {
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
| `id` | string | yes | Reporting batch ID. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `status` | string | no | Filter batch items by status, e.g. Completed. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "continuationToken": "string",
      "results": [
        {
          "batchId": "string",
          "createdOn": "2026-05-07T12:00:00.000Z",
          "cvr": 1,
          "format": "string",
          "id": "string",
          "internalCustomerId": 1,
          "name": "Ava Chen",
          "pdfurl": "https://example.com",
          "printType": "string",
          "status": "string"
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
| `continuationToken` | string |  |
| `results[].batchId` | string |  |
| `results[].createdOn` | date |  |
| `results[].cvr` | number |  |
| `results[].format` | string |  |
| `results[].id` | string |  |
| `results[].internalCustomerId` | number |  |
| `results[].name` | string |  |
| `results[].pdfurl` | string |  |
| `results[].printType` | string |  |
| `results[].status` | string |  |

## Native endpoint

Through the native Lasso X API, this operation is `GET /apps/reporting/batches/:id/items` (base URL `https://api.lassox.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-reporting-batch-items.md) for the provider-specific parameters and requirements.

