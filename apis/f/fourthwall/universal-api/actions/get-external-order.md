# Fourthwall: Get External Order

Retrieves an external order from Fourthwall by source and ID.

```
GET https://connect.mindcloud.co/v1/universal/fourthwall/latest/actions/get-external-order
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Fourthwall `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fourthwall/latest/actions/get-external-order?connectionId=$CONNECTION_ID&externalSource=string&externalOrderId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "externalSource": "string",
  "externalOrderId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fourthwall/latest/actions/get-external-order?${params}`, {
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
| `externalSource` | string | yes | The external order source. |
| `externalOrderId` | string | yes | The external order ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "2026-05-07T12:00:00.000Z",
      "externalOrderId": "string",
      "externalSource": "string",
      "friendlyId": "string",
      "orderId": "string",
      "status": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date |  |
| `externalOrderId` | string |  |
| `externalSource` | string |  |
| `friendlyId` | string |  |
| `orderId` | string |  |
| `status` | string |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native Fourthwall API, this operation is `GET /open-api/v1.0/external-orders/:externalSource/:externalOrderId` (base URL `https://api.fourthwall.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-external-order.md) for the provider-specific parameters and requirements.

