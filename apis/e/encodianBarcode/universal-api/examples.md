# Encodian - Barcode Universal API Examples

These examples use the MindCloud API key and Encodian - Barcode connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Barcode - Read Document Status



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/encodianBarcode/latest/actions/barcode-read-document-status?connectionId=$CONNECTION_ID&operationId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "operationId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/encodianBarcode/latest/actions/barcode-read-document-status?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

Example response:

```json
{
  "success": true,
  "data": [
    {
      "barcodes": [
        "string"
      ],
      "Errors": [
        "string"
      ],
      "HttpStatusCode": 1,
      "HttpStatusMessage": "string",
      "OperationId": "string",
      "OperationStatus": "string"
    }
  ],
  "meta": {}
}
```

See the full [Barcode - Read Document Status action reference](actions/barcode-read-document-status.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/encodianBarcode/latest/actions/barcode-read-document-status).

## Barcode - Create



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/encodianBarcode/latest/actions/barcode-create" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "barcodeType": "0",
  "barcodeData": "string",
  "barcodeImageFormat": "0"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/encodianBarcode/latest/actions/barcode-create', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "barcodeType": "0",
    "barcodeData": "string",
    "barcodeImageFormat": "0"
  })
});

const { success, data } = await response.json();
```

Example response:

```json
{
  "success": true,
  "data": [
    {
      "Errors": [
        "string"
      ],
      "FileContent": "string",
      "Filename": "Ava Chen",
      "HttpStatusCode": 1,
      "HttpStatusMessage": "string",
      "OperationId": "string",
      "OperationStatus": "string"
    }
  ],
  "meta": {}
}
```

See the full [Barcode - Create action reference](actions/barcode-create.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/encodianBarcode/latest/actions/barcode-create).
