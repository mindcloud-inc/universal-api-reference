# Encodian - Barcode: Swiss QR Code - Create



```
POST https://connect.mindcloud.co/v1/universal/encodianBarcode/latest/actions/swiss-qr-code-create
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Encodian - Barcode `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/encodianBarcode/latest/actions/swiss-qr-code-create" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "imageFormat": "0",
  "account": "string",
  "currency": "0",
  "amount": 1,
  "reference": "string",
  "creditor": {},
  "debtor": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/encodianBarcode/latest/actions/swiss-qr-code-create', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "imageFormat": "0",
    "account": "string",
    "currency": "0",
    "amount": 1,
    "reference": "string",
    "creditor": {},
    "debtor": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `imageFormat` | string | yes | Output image format of the Swiss QR code. One of: `0`, `1`, `2`, `3`, `4`, `5`. |
| `account` | string | yes | Creditor IBAN or account value for the Swiss QR code. |
| `currency` | string | yes | Payment currency. One of: `0`, `1`. |
| `amount` | number | yes | Payment amount. |
| `reference` | string | yes | Swiss QR payment reference value. |
| `creditor` | object | yes | Creditor object containing name and address fields. |
| `debtor` | object | yes | Debtor object containing name and address fields. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `width` | number | no | Swiss QR code width in pixels. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "Errors": [
        "string"
      ],
      "FileContent": "string",
      "HttpStatusCode": 1,
      "HttpStatusMessage": "string",
      "OperationId": "string",
      "OperationStatus": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `Errors` | array<string> | Error messages returned by Encodian. |
| `FileContent` | string | Generated Swiss QR code image file content. |
| `HttpStatusCode` | number | HTTP status code returned by Encodian. |
| `HttpStatusMessage` | string | HTTP status message returned by Encodian. |
| `OperationId` | string | Encodian operation identifier. |
| `OperationStatus` | string | Encodian operation status. |

## Native endpoint

Through the native Encodian - Barcode API, this operation is `POST /api/v1/Barcodes/CreateSwissQrCode` (base URL `https://api.apps-encodian.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/swiss-qr-code-create.md) for the provider-specific parameters and requirements.

