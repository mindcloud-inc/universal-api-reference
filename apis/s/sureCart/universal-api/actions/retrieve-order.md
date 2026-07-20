# SureCart: Retrieve Order



```
GET https://connect.mindcloud.co/v1/universal/sureCart/latest/actions/retrieve-order
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SureCart `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sureCart/latest/actions/retrieve-order?connectionId=$CONNECTION_ID&id=d860470d-c697-4a0c-9749-59cd5ac2ec4e" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "d860470d-c697-4a0c-9749-59cd5ac2ec4e"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sureCart/latest/actions/retrieve-order?${params}`, {
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
| `id` | string | yes | The order ID to retrieve. Example: `d860470d-c697-4a0c-9749-59cd5ac2ec4e`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "checkout": "string",
      "createdAt": 1,
      "fulfillmentStatus": "string",
      "id": "string",
      "liveMode": true,
      "number": "string",
      "object": "string",
      "orderType": "string",
      "pdfUrl": "https://example.com",
      "portalUrl": "https://example.com",
      "returnStatus": "string",
      "shipmentStatus": "string",
      "statementUrl": "https://example.com",
      "status": "string",
      "updatedAt": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `checkout` | string |  |
| `createdAt` | number |  |
| `fulfillmentStatus` | string |  |
| `id` | string |  |
| `liveMode` | boolean |  |
| `number` | string |  |
| `object` | string |  |
| `orderType` | string |  |
| `pdfUrl` | string |  |
| `portalUrl` | string |  |
| `returnStatus` | string |  |
| `shipmentStatus` | string |  |
| `statementUrl` | string |  |
| `status` | string |  |
| `updatedAt` | number |  |

## Native endpoint

Through the native SureCart API, this operation is `GET v1/orders/:id` (base URL `https://api.surecart.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-order.md) for the provider-specific parameters and requirements.

