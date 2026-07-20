# Halo Service Solutions: Get Invoice

Retrieves an invoice from Halo Service Solutions.

```
GET https://connect.mindcloud.co/v1/universal/haloServiceSolutions/latest/actions/get-invoice
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Halo Service Solutions `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/haloServiceSolutions/latest/actions/get-invoice?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/haloServiceSolutions/latest/actions/get-invoice?${params}`, {
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
| `id` | number | yes | Invoice ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "add_salesorder": 1,
      "amountdue": 1,
      "assigned_agent": 1,
      "client_id": 1,
      "client_name": "Ava Chen",
      "duedate": "2026-05-07T12:00:00.000Z",
      "id": 1,
      "internal_note": "string",
      "invoice_date": "2026-05-07T12:00:00.000Z",
      "name": "Ava Chen",
      "paymentstatus": 1,
      "site_name": "Ava Chen",
      "sitenumber": 1,
      "total": 1,
      "uid": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `add_salesorder` | number |  |
| `amountdue` | number |  |
| `assigned_agent` | number |  |
| `client_id` | number |  |
| `client_name` | string |  |
| `duedate` | date |  |
| `id` | number | Invoice ID |
| `internal_note` | string |  |
| `invoice_date` | date |  |
| `name` | string |  |
| `paymentstatus` | number |  |
| `site_name` | string |  |
| `sitenumber` | number |  |
| `total` | number |  |
| `uid` | number |  |

## Native endpoint

Through the native Halo Service Solutions API, this operation is `GET /Invoice/:id` (base URL `https://mindcloud.halopsa.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-invoice.md) for the provider-specific parameters and requirements.

