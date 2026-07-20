# Shipcloud: Get Shipment Document

Retrieves a shipment document from Shipcloud by ID.

```
GET https://connect.mindcloud.co/v1/universal/shipcloud/latest/actions/get-shipment-document
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Shipcloud `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/shipcloud/latest/actions/get-shipment-document?connectionId=$CONNECTION_ID&shipmentDocumentId=string&shipmentId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "shipmentDocumentId": "string",
  "shipmentId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/shipcloud/latest/actions/get-shipment-document?${params}`, {
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
| `shipmentDocumentId` | string | yes | The Shipcloud shipment document identifier. |
| `shipmentId` | string | yes | The Shipcloud shipment identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "document_format": "string",
      "document_type": "string",
      "document_url": "https://example.com",
      "id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `document_format` | string |  |
| `document_type` | string |  |
| `document_url` | string |  |
| `id` | string |  |

## Native endpoint

Through the native Shipcloud API, this operation is `GET /shipments/:shipmentId/shipment_documents/:shipmentDocumentId` (base URL `https://api.shipcloud.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-shipment-document.md) for the provider-specific parameters and requirements.

