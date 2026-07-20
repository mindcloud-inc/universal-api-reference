# SWELLEnterprise: Create Estimate

Creates a new estimate in SWELLEnterprise.

```
POST https://connect.mindcloud.co/v1/universal/sWELLEnterprise/latest/actions/create-estimate
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SWELLEnterprise `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/sWELLEnterprise/latest/actions/create-estimate" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/sWELLEnterprise/latest/actions/create-estimate', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `contactId` | number | no | The contact ID. |
| `companyId` | number | no | The company ID. |
| `status` | string | no | The estimate status. |
| `validUntil` | date | no | The expiration date. |
| `subtotal` | number | no | The subtotal amount. |
| `taxRate` | number | no | The tax rate percentage. |
| `currency` | string | no | The currency code. |
| `notes` | string | no | Additional notes. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "companyId": 1,
        "contactId": 1,
        "currency": "string",
        "estimateNumber": "string",
        "id": 1,
        "notes": "string",
        "status": "string",
        "subtotal": "string",
        "taxRate": "string",
        "validUntil": "2026-05-07T12:00:00.000Z"
      },
      "message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data.companyId` | number | The linked company ID. |
| `data.contactId` | number | The linked contact ID. |
| `data.currency` | string | The currency code. |
| `data.estimateNumber` | string | The estimate number. |
| `data.id` | number | The estimate ID. |
| `data.notes` | string | Additional notes. |
| `data.status` | string | The estimate status. |
| `data.subtotal` | string | The subtotal amount. |
| `data.taxRate` | string | The tax rate percentage. |
| `data.validUntil` | date | The expiration date. |
| `message` | string | Success message. |

## Native endpoint

Through the native SWELLEnterprise API, this operation is `POST /finance/estimates` (base URL `https://dashboard.swellsystem.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-estimate.md) for the provider-specific parameters and requirements.

