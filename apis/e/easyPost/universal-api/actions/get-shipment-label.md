# EasyPost: Get Shipment Label

Retrieves a label for a shipment from EasyPost.

```
GET https://connect.mindcloud.co/v1/universal/easyPost/latest/actions/get-shipment-label
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a EasyPost `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/easyPost/latest/actions/get-shipment-label?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/easyPost/latest/actions/get-shipment-label?${params}`, {
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
| `id` | string | yes | EasyPost Shipment ID, beginning with shp_. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "labelEpl2Url": "https://example.com",
      "labelFileType": "string",
      "labelPdfUrl": "https://example.com",
      "labelUrl": "https://example.com",
      "labelZplUrl": "https://example.com",
      "object": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |
| `labelEpl2Url` | string |  |
| `labelFileType` | string |  |
| `labelPdfUrl` | string |  |
| `labelUrl` | string |  |
| `labelZplUrl` | string |  |
| `object` | string |  |

## Native endpoint

Through the native EasyPost API, this operation is `GET /shipments/:id/label` (base URL `https://api.easypost.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-shipment-label.md) for the provider-specific parameters and requirements.

