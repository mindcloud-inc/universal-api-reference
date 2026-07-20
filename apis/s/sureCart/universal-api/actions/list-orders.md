# SureCart: List Orders



```
GET https://connect.mindcloud.co/v1/universal/sureCart/latest/actions/list-orders
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SureCart `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sureCart/latest/actions/list-orders?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sureCart/latest/actions/list-orders?${params}`, {
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
| `liveMode` | boolean | no | Only return live mode or test mode orders. |
| `query` | string | no | Full-text search query for the order collection. Example: `0001`. |

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

Through the native SureCart API, this operation is `GET v1/orders` (base URL `https://api.surecart.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-orders.md) for the provider-specific parameters and requirements.

