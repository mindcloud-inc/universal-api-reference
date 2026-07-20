# Encodian - Barcode: Swiss QR Code - Read from Image



```
GET https://connect.mindcloud.co/v1/universal/encodianBarcode/latest/actions/swiss-qr-code-read-from-image
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Encodian - Barcode `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/encodianBarcode/latest/actions/swiss-qr-code-read-from-image?connectionId=$CONNECTION_ID&fileContent=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "fileContent": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/encodianBarcode/latest/actions/swiss-qr-code-read-from-image?${params}`, {
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
| `fileContent` | string | yes | Base64 source image file content. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `barcodeRemoveControlChars` | boolean | no | Remove recognized control characters from decoded values. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "account": "string",
      "amount": 1,
      "creditorAddressLine1": "string",
      "creditorAddressLine2": "string",
      "creditorCountryCode": "string",
      "creditorHouseNo": "string",
      "creditorName": "Ava Chen",
      "creditorPostcode": "string",
      "creditorStreet": "string",
      "creditorTown": "string",
      "currency": "string",
      "debtorAddressLine1": "string",
      "debtorAddressLine2": "string",
      "debtorCountryCode": "string",
      "debtorHouseNo": "string",
      "debtorName": "Ava Chen",
      "debtorPostcode": "string",
      "debtorStreet": "string",
      "debtorTown": "string",
      "Errors": [
        "string"
      ],
      "HttpStatusCode": 1,
      "HttpStatusMessage": "string",
      "OperationId": "string",
      "OperationStatus": "string",
      "reference": "string",
      "value": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `account` | string | Account from the Swiss QR code. |
| `amount` | number | Amount from the Swiss QR code. |
| `creditorAddressLine1` | string | Creditor address line 1 from the Swiss QR code. |
| `creditorAddressLine2` | string | Creditor address line 2 from the Swiss QR code. |
| `creditorCountryCode` | string | Creditor country code from the Swiss QR code. |
| `creditorHouseNo` | string | Creditor house number from the Swiss QR code. |
| `creditorName` | string | Creditor name from the Swiss QR code. |
| `creditorPostcode` | string | Creditor postal code from the Swiss QR code. |
| `creditorStreet` | string | Creditor street from the Swiss QR code. |
| `creditorTown` | string | Creditor town from the Swiss QR code. |
| `currency` | string | Currency from the Swiss QR code. |
| `debtorAddressLine1` | string | Debtor address line 1 from the Swiss QR code. |
| `debtorAddressLine2` | string | Debtor address line 2 from the Swiss QR code. |
| `debtorCountryCode` | string | Debtor country code from the Swiss QR code. |
| `debtorHouseNo` | string | Debtor house number from the Swiss QR code. |
| `debtorName` | string | Debtor name from the Swiss QR code. |
| `debtorPostcode` | string | Debtor postal code from the Swiss QR code. |
| `debtorStreet` | string | Debtor street from the Swiss QR code. |
| `debtorTown` | string | Debtor town from the Swiss QR code. |
| `Errors` | array<string> | Error messages returned by Encodian. |
| `HttpStatusCode` | number | HTTP status code. |
| `HttpStatusMessage` | string | HTTP status message. |
| `OperationId` | string | Operation ID. |
| `OperationStatus` | string | Encodian operation status. |
| `reference` | string | Reference from the Swiss QR code. |
| `value` | string | Decoded Swiss QR code value. |

## Native endpoint

Through the native Encodian - Barcode API, this operation is `POST /api/v1/Barcodes/ReadSwissQrCodeFromImage` (base URL `https://api.apps-encodian.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/swiss-qr-code-read-from-image.md) for the provider-specific parameters and requirements.

