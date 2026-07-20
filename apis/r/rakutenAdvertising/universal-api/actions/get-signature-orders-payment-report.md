# Rakuten Advertising: Get signature orders payment report

Retrieves a signature orders payment report from Rakuten Advertising.

```
GET https://connect.mindcloud.co/v1/universal/rakutenAdvertising/latest/actions/get-signature-orders-payment-report
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rakuten Advertising `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rakutenAdvertising/latest/actions/get-signature-orders-payment-report?connectionId=$CONNECTION_ID&payid=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "payid": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rakutenAdvertising/latest/actions/get-signature-orders-payment-report?${params}`, {
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
| `payid` | string | yes | Rakuten payment ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "advertiserId": "string",
      "advertiserName": "Ava Chen",
      "commission": 1,
      "currency": "string",
      "orderAmount": 1,
      "orderId": "string",
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
| `commission` | number |  |
| `currency` | string |  |
| `orderAmount` | number |  |
| `orderId` | string |  |
| `paymentId` | string |  |
| `rawRow` | object |  |
| `reportId` | string |  |

## Native endpoint

Through the native Rakuten Advertising API, this operation is `GET /advancedreports/1.0` (base URL `https://api.linksynergy.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-signature-orders-payment-report.md) for the provider-specific parameters and requirements.

