# Rillion Prime Web Service: Count Account Coded Invoices

Count how many times an invoice has been account coded.

```
GET https://connect.mindcloud.co/v1/universal/rillionPrimeWebService/latest/actions/count-account-coded-invoices
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rillion Prime Web Service `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rillionPrimeWebService/latest/actions/count-account-coded-invoices?connectionId=$CONNECTION_ID&invoiceSeries=string&invoiceNo=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "invoiceSeries": "string",
  "invoiceNo": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rillionPrimeWebService/latest/actions/count-account-coded-invoices?${params}`, {
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
| `invoiceSeries` | string | yes | Invoice series of the invoice. |
| `invoiceNo` | number | yes | Invoice number of the invoice. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "result": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `result` | string | Number of times the invoice has been account coded. |

## Native endpoint

Through the native Rillion Prime Web Service API, this operation is `POST` (base URL `{{credentials.baseUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/count-account-coded-invoices.md) for the provider-specific parameters and requirements.

