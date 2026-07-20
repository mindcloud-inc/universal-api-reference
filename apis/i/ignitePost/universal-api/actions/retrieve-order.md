# IgnitePost: Retrieve Order

Retrieves an existing order from IgnitePost.

```
GET https://connect.mindcloud.co/v1/universal/ignitePost/latest/actions/retrieve-order
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a IgnitePost `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ignitePost/latest/actions/retrieve-order?connectionId=$CONNECTION_ID&orderId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "orderId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ignitePost/latest/actions/retrieve-order?${params}`, {
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
| `orderId` | string | yes | The IgnitePOST order ID to retrieve. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "2026-05-07T12:00:00.000Z",
      "font": "string",
      "id": "string",
      "imageBacksideUrl": "https://example.com",
      "imageInsideUrl": "https://example.com",
      "imageUrl": "https://example.com",
      "insert": "string",
      "message": "string",
      "metadata": {},
      "recipientAddressOne": "string",
      "recipientAddressTwo": "string",
      "recipientCity": "string",
      "recipientCompanyName": "Ava Chen",
      "recipientEmail": "ava@example.com",
      "recipientName": "Ava Chen",
      "recipientState": "string",
      "recipientZip": "string",
      "senderAddressOne": "string",
      "senderAddressTwo": "string",
      "senderCity": "string",
      "senderName": "Ava Chen",
      "senderState": "string",
      "senderZip": "string",
      "sendOn": "2026-05-07T12:00:00.000Z",
      "sentAt": "2026-05-07T12:00:00.000Z",
      "uid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date | Timestamp when the order was created. |
| `font` | string | IgnitePost font key. |
| `id` | string | Unique identifier for the order. |
| `imageBacksideUrl` | string | Backside image URL. |
| `imageInsideUrl` | string | Inside image URL. |
| `imageUrl` | string | Front image URL. |
| `insert` | string | Optional insert key. |
| `message` | string | Handwritten letter text. |
| `metadata` | object | Arbitrary order metadata returned by IgnitePost. |
| `recipientAddressOne` | string | Recipient address line 1. |
| `recipientAddressTwo` | string | Recipient address line 2. |
| `recipientCity` | string | Recipient city. |
| `recipientCompanyName` | string | Recipient company name. |
| `recipientEmail` | string | Recipient email. |
| `recipientName` | string | Recipient name. |
| `recipientState` | string | Recipient state. |
| `recipientZip` | string | Recipient ZIP or postal code. |
| `senderAddressOne` | string | Sender address line 1. |
| `senderAddressTwo` | string | Sender address line 2. |
| `senderCity` | string | Sender city. |
| `senderName` | string | Sender name. |
| `senderState` | string | Sender state. |
| `senderZip` | string | Sender ZIP or postal code. |
| `sendOn` | date | Scheduled send date. |
| `sentAt` | date | Timestamp when the order was sent. |
| `uid` | string | External identifier from the calling system. |

## Native endpoint

Through the native IgnitePost API, this operation is `GET /orders/:id` (base URL `https://dashboard.ignitepost.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-order.md) for the provider-specific parameters and requirements.

