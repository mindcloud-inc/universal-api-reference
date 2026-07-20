# Rakuten Advertising: Get invoice report

Retrieves an invoice report from Rakuten Advertising.

```
GET https://connect.mindcloud.co/v1/universal/rakutenAdvertising/latest/actions/get-invoice-report
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rakuten Advertising `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rakutenAdvertising/latest/actions/get-invoice-report?connectionId=$CONNECTION_ID&invoiceid=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "invoiceid": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rakutenAdvertising/latest/actions/get-invoice-report?${params}`, {
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
| `invoiceid` | string | yes | Rakuten invoice ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "advertiserId": "string",
      "advertiserName": "Ava Chen",
      "currency": "string",
      "invoiceAmount": 1,
      "invoiceId": "string",
      "paymentId": "string",
      "rawRow": {},
      "reportId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `advertiserId` | string |  |
| `advertiserName` | string |  |
| `currency` | string |  |
| `invoiceAmount` | number |  |
| `invoiceId` | string |  |
| `paymentId` | string |  |
| `rawRow` | object |  |
| `reportId` | string |  |

## Native endpoint

Through the native Rakuten Advertising API, this operation is `GET /advancedreports/1.0` (base URL `https://api.linksynergy.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-invoice-report.md) for the provider-specific parameters and requirements.

