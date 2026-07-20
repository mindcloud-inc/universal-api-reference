# Bitskout: Extract Data from Purchase Order

Extracts purchase order data with a Bitskout plugin.

```
POST https://connect.mindcloud.co/v1/universal/bitskout/latest/actions/extract-data-from-purchase-order
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bitskout `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/bitskout/latest/actions/extract-data-from-purchase-order" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/bitskout/latest/actions/extract-data-from-purchase-order', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `fileUrl` | string | no | Download URL for the purchase order file to extract. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "outputs": {
        "ACCOUNT_NUMBER": "string",
        "CUSTOMER_NAME": "Ava Chen",
        "LINE_ITEMS": "string",
        "name": "Ava Chen",
        "NUMBER_OF_PAGES": 1,
        "PURCHASE_ORDER_DATE": "string",
        "PURCHASE_ORDER_ID": "string",
        "PURCHASE_ORDER_NUMBER": "string",
        "RawJSON": "string",
        "RECEIVER_ADDRESS": "string",
        "RECEIVER_NAME": "Ava Chen",
        "REFERENCE_NUMBER": "string",
        "TAX_ID": "string",
        "TOTAL": "string",
        "TRACKING_NUMBER": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `outputs` | object | Purchase order extraction outputs |
| `outputs.ACCOUNT_NUMBER` | string | Account Number |
| `outputs.CUSTOMER_NAME` | string | Customer Name |
| `outputs.LINE_ITEMS` | string | Line Items as CSV |
| `outputs.name` | string | File Name |
| `outputs.NUMBER_OF_PAGES` | number | Number of Pages in the Document |
| `outputs.PURCHASE_ORDER_DATE` | string | Purchase Order Date |
| `outputs.PURCHASE_ORDER_ID` | string | Purchase Order ID |
| `outputs.PURCHASE_ORDER_NUMBER` | string | Purchase Order Number |
| `outputs.RawJSON` | string | Raw JSON |
| `outputs.RECEIVER_ADDRESS` | string | Receiver's Address |
| `outputs.RECEIVER_NAME` | string | Receiver's Name |
| `outputs.REFERENCE_NUMBER` | string | Reference Number |
| `outputs.TAX_ID` | string | Tax ID |
| `outputs.TOTAL` | string | Total |
| `outputs.TRACKING_NUMBER` | string | Tracking Number |

## Native endpoint

Through the native Bitskout API, this operation is `POST /actions/purchase_order` (base URL `https://api.bitskout.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/extract-data-from-purchase-order.md) for the provider-specific parameters and requirements.

