# Prerender.io: List Billing Invoices

Retrieves billing invoices from Prerender.io.

```
GET https://connect.mindcloud.co/v1/universal/prerenderio/latest/actions/get-v3-billing-invoices
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Prerender.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/prerenderio/latest/actions/get-v3-billing-invoices?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/prerenderio/latest/actions/get-v3-billing-invoices?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "amountPaidInCent": 1,
      "date": "string",
      "dueDate": "string",
      "extraCostInCent": 1,
      "extraRenders": 1,
      "id": "string",
      "includedRenders": 1,
      "isPackageOnly": true,
      "packages": [
        "string"
      ],
      "paidAt": "string",
      "planCostInCent": 1,
      "planName": "Ava Chen",
      "renders": 1,
      "status": "string",
      "totalInCent": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `amountPaidInCent` | number |  |
| `date` | string |  |
| `dueDate` | string |  |
| `extraCostInCent` | number |  |
| `extraRenders` | number |  |
| `id` | string |  |
| `includedRenders` | number |  |
| `isPackageOnly` | boolean |  |
| `packages` | array<string> |  |
| `paidAt` | string |  |
| `planCostInCent` | number |  |
| `planName` | string |  |
| `renders` | number |  |
| `status` | string |  |
| `totalInCent` | number |  |

## Native endpoint

Through the native Prerender.io API, this operation is `GET /v3/billing/invoices` (base URL `https://api.prerender.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-v3-billing-invoices.md) for the provider-specific parameters and requirements.

