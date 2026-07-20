# EasyPost: Get Refund

Retrieves details for a refund from EasyPost.

```
GET https://connect.mindcloud.co/v1/universal/easyPost/latest/actions/get-refund
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a EasyPost `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/easyPost/latest/actions/get-refund?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/easyPost/latest/actions/get-refund?${params}`, {
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
| `id` | string | yes | EasyPost Refund ID, beginning with rfnd_. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "carrier": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "mode": "string",
      "object": "string",
      "shipmentId": "string",
      "status": "string",
      "trackingCode": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `carrier` | string |  |
| `createdAt` | date |  |
| `id` | string |  |
| `mode` | string |  |
| `object` | string |  |
| `shipmentId` | string |  |
| `status` | string |  |
| `trackingCode` | string |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native EasyPost API, this operation is `GET /refunds/:id` (base URL `https://api.easypost.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-refund.md) for the provider-specific parameters and requirements.

