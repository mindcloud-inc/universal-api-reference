# Billingo: Create Document Export

Creates a new document export in Billingo.

```
POST https://connect.mindcloud.co/v1/universal/billingo/latest/actions/create-document-export
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Billingo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/billingo/latest/actions/create-document-export" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "queryType": "invoice_date",
  "startDate": "2026-01-01",
  "endDate": "2026-01-31",
  "exportType": "simple_csv"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/billingo/latest/actions/create-document-export', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "queryType": "invoice_date",
    "startDate": "2026-01-01",
    "endDate": "2026-01-31",
    "exportType": "simple_csv"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `queryType` | string | yes | Date field used for the export range. One of: `0`, `1`, `2`, `3`. Default: `invoice_date`. |
| `startDate` | date | yes | Start date for the export range. Default: `2026-01-01`. |
| `endDate` | date | yes | End date for the export range. Default: `2026-01-31`. |
| `exportType` | string | yes | Billingo export format/type. Default: `simple_csv`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | number | Document export job ID. |

## Native endpoint

Through the native Billingo API, this operation is `POST /document-export` (base URL `https://api.billingo.hu/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-document-export.md) for the provider-specific parameters and requirements.

