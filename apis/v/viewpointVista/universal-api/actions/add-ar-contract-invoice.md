# Viewpoint Vista: Add AR Contract Invoice

Adds a Contract based invoice.

```
POST https://connect.mindcloud.co/v1/universal/viewpointVista/latest/actions/add-ar-contract-invoice
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Viewpoint Vista `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/viewpointVista/latest/actions/add-ar-contract-invoice" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "co": 1,
  "mth": "2026-05-01",
  "BatchId": 1,
  "CustGroup": 1,
  "Customer": 1,
  "JCCo": 1,
  "Contract": "string",
  "TransDate": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/viewpointVista/latest/actions/add-ar-contract-invoice', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "co": 1,
    "mth": "2026-05-01",
    "BatchId": 1,
    "CustGroup": 1,
    "Customer": 1,
    "JCCo": 1,
    "Contract": "string",
    "TransDate": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `co` | number | yes | Vista PR company. |
| `mth` | string | yes | Posting month for the batch. Format: YYYY-MM-DD. Example: `2026-05-01`. |
| `BatchId` | number | yes |  |
| `CustGroup` | number | yes |  |
| `Customer` | number | yes |  |
| `RecType` | number | no |  |
| `CustRef` | string | no |  |
| `JCCo` | number | yes |  |
| `Contract` | string | yes |  |
| `CustRef` | string | no |  |
| `Invoice` | string | no |  |
| `Description` | string | no |  |
| `TransDate` | string | yes |  |
| `DueDate` | string | no |  |
| `DiscDate` | string | no |  |
| `ReasonCode` | string | no |  |
| `Notes` | string | no |  |
| `__custom_fields` | object | no |  |
| `MiscDistributions[]` | array | no |  |
| `LineItems[]` | array | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "operation": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |
| `operation` | string |  |
| `status` | string |  |

## Native endpoint

Through the native Viewpoint Vista API, this operation is `POST v1/direct/subscribers/{{credentials.subscriberCode}}/vista/ar/2/data/batch_entries/actions/add_contract_inv_v2` (base URL `https://api.xchange.trimble.com/connect/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-ar-contract-invoice.md) for the provider-specific parameters and requirements.

