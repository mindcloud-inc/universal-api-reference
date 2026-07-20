# IgnitePost: Create Order

Creates a new order in IgnitePost.

```
POST https://connect.mindcloud.co/v1/universal/ignitePost/latest/actions/create-order
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a IgnitePost `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/ignitePost/latest/actions/create-order" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "font": "string",
  "message": "string",
  "image": "string",
  "recipientAddressOne": "string",
  "recipientCity": "string",
  "recipientState": "string",
  "recipientZip": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/ignitePost/latest/actions/create-order', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "font": "string",
    "message": "string",
    "image": "string",
    "recipientAddressOne": "string",
    "recipientCity": "string",
    "recipientState": "string",
    "recipientZip": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `font` | string | yes | IgnitePOST font key from the List Fonts action. |
| `message` | string | yes | Handwritten message content, up to 450 characters. |
| `image` | string | yes | Front image key from List Default Images or a public image URL. |
| `imageInside` | string | no | A stock image key or image URL for the card interior. |
| `imageBackside` | string | no | A stock image key or image URL for the card back. |
| `insert` | string | no | An optional IgnitePOST insert key, such as a gift card insert. |
| `recipientName` | string | no | Recipient full name. |
| `recipientEmail` | string | no | Recipient email address for delivery notifications. |
| `recipientCompanyName` | string | no | Recipient company name for business deliveries. |
| `recipientAddressOne` | string | yes | Recipient street address line 1. |
| `recipientAddressTwo` | string | no | Recipient street address line 2, such as a suite or apartment. |
| `recipientCity` | string | yes | Recipient city. |
| `recipientState` | string | yes | Recipient state or region code. |
| `recipientZip` | string | yes | Recipient ZIP or postal code. |
| `senderName` | string | no | Sender name shown on the card. |
| `senderAddressOne` | string | no | Sender street address line 1. |
| `senderAddressTwo` | string | no | Sender street address line 2, such as a suite or apartment. |
| `senderCity` | string | no | Sender city. |
| `senderState` | string | no | Sender state or region code. |
| `senderZip` | string | no | Sender ZIP or postal code. |
| `sendOn` | date | no | Schedule the order for a future send date in YYYY-MM-DD format. |
| `letterTemplateId` | number | no | Letter template ID from the List Letter Templates action. |
| `uid` | string | no | Your external unique identifier for the order. |
| `metadata` | object | no | Object of key-value metadata to attach to the order. |

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
      "letterTemplateId": 1,
      "message": "string",
      "metadata": {},
      "recipientAddressOne": "string",
      "recipientAddressTwo": "string",
      "recipientCity": "string",
      "recipientCompanyName": "Ava Chen",
      "recipientCountry": "string",
      "recipientEmail": "ava@example.com",
      "recipientName": "Ava Chen",
      "recipientState": "string",
      "recipientZip": "string",
      "senderAddressOne": "string",
      "senderAddressTwo": "string",
      "senderCity": "string",
      "senderCountry": "string",
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
| `letterTemplateId` | number | Template identifier returned on the observed create-order response. |
| `message` | string | Handwritten letter text. |
| `metadata` | object | Arbitrary order metadata returned by IgnitePost. |
| `recipientAddressOne` | string | Recipient address line 1. |
| `recipientAddressTwo` | string | Recipient address line 2. |
| `recipientCity` | string | Recipient city. |
| `recipientCompanyName` | string | Recipient company name. |
| `recipientCountry` | string | Recipient country code returned on the observed create-order response. |
| `recipientEmail` | string | Recipient email. |
| `recipientName` | string | Recipient name. |
| `recipientState` | string | Recipient state. |
| `recipientZip` | string | Recipient ZIP or postal code. |
| `senderAddressOne` | string | Sender address line 1. |
| `senderAddressTwo` | string | Sender address line 2. |
| `senderCity` | string | Sender city. |
| `senderCountry` | string | Sender country code returned on the observed create-order response. |
| `senderName` | string | Sender name. |
| `senderState` | string | Sender state. |
| `senderZip` | string | Sender ZIP or postal code. |
| `sendOn` | date | Scheduled send date. |
| `sentAt` | date | Timestamp when the order was sent. |
| `uid` | string | External identifier from the calling system. |

## Native endpoint

Through the native IgnitePost API, this operation is `POST /orders` (base URL `https://dashboard.ignitepost.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-order.md) for the provider-specific parameters and requirements.

