# EasyPost: Create Refund

Creates a new refund in EasyPost.

```
POST https://connect.mindcloud.co/v1/universal/easyPost/latest/actions/create-refund
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a EasyPost `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/easyPost/latest/actions/create-refund" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "refund": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/easyPost/latest/actions/create-refund', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "refund": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `refund` | object | yes | Refund request object to create. |

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

Through the native EasyPost API, this operation is `POST /refunds` (base URL `https://api.easypost.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-refund.md) for the provider-specific parameters and requirements.

