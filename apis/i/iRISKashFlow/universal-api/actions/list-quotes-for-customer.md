# IRIS KashFlow: List Quotes for Customer



```
GET https://connect.mindcloud.co/v1/universal/iRISKashFlow/latest/actions/list-quotes-for-customer
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a IRIS KashFlow `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/iRISKashFlow/latest/actions/list-quotes-for-customer?connectionId=$CONNECTION_ID&customerId=98598416" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "customerId": "98598416"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/iRISKashFlow/latest/actions/list-quotes-for-customer?${params}`, {
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
| `customerId` | number | yes | Default: `98598416`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "amountPaid": "string",
      "cISRCNetAmount": "string",
      "cISRCVatAmount": "string",
      "customerID": "string",
      "dueDate": "string",
      "exchangeRate": "string",
      "invoiceDate": "string",
      "invoiceDBID": "string",
      "invoiceNumber": "string",
      "isCISReverseCharge": "string",
      "lines": "string",
      "netAmount": "string",
      "paid": "string",
      "projectID": "string",
      "readableString": "string",
      "suppressTotal": "string",
      "useCustomDeliveryAddress": "string",
      "vATAmount": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `amountPaid` | string |  |
| `cISRCNetAmount` | string |  |
| `cISRCVatAmount` | string |  |
| `customerID` | string |  |
| `dueDate` | string |  |
| `exchangeRate` | string |  |
| `invoiceDate` | string |  |
| `invoiceDBID` | string |  |
| `invoiceNumber` | string |  |
| `isCISReverseCharge` | string |  |
| `lines` | string |  |
| `netAmount` | string |  |
| `paid` | string |  |
| `projectID` | string |  |
| `readableString` | string |  |
| `suppressTotal` | string |  |
| `useCustomDeliveryAddress` | string |  |
| `vATAmount` | string |  |

## Native endpoint

Through the native IRIS KashFlow API, this operation is `POST /api/service.asmx` (base URL `https://securedwebapp.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-quotes-for-customer.md) for the provider-specific parameters and requirements.

