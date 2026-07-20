# Pushover: Get Receipt Status



```
GET https://connect.mindcloud.co/v1/universal/pushover/latest/actions/get-receipt-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pushover `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pushover/latest/actions/get-receipt-status?connectionId=$CONNECTION_ID&receipt=p3v6Q9x2Lm4N8c1R5t7Y0z2Aa4Bb6C" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "receipt": "p3v6Q9x2Lm4N8c1R5t7Y0z2Aa4Bb6C"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pushover/latest/actions/get-receipt-status?${params}`, {
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
| `receipt` | string | yes | Emergency notification receipt to inspect. Example: `p3v6Q9x2Lm4N8c1R5t7Y0z2Aa4Bb6C`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "acknowledged": 1,
      "acknowledgedAt": 1,
      "acknowledgedBy": "string",
      "acknowledgedByDevice": "string",
      "calledBack": 1,
      "calledBackAt": 1,
      "expired": 1,
      "expiresAt": 1,
      "lastDeliveredAt": 1,
      "request": "string",
      "status": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `acknowledged` | number | Whether the emergency notification has been acknowledged. |
| `acknowledgedAt` | number | Unix timestamp for when the notification was acknowledged, or 0. |
| `acknowledgedBy` | string | User key that first acknowledged the notification. |
| `acknowledgedByDevice` | string | Device name that first acknowledged the notification. |
| `calledBack` | number | Whether the callback URL has been invoked. |
| `calledBackAt` | number | Unix timestamp for when the callback URL was invoked, or 0. |
| `expired` | number | Whether the receipt has expired. |
| `expiresAt` | number | Unix timestamp for when the receipt expires. |
| `lastDeliveredAt` | number | Unix timestamp of the last delivery attempt, or 0. |
| `request` | string | Pushover request identifier. |
| `status` | number | API status. Returns 1 when the receipt lookup succeeds. |

## Native endpoint

Through the native Pushover API, this operation is `GET /receipts/:receipt.json` (base URL `https://api.pushover.net/1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-receipt-status.md) for the provider-specific parameters and requirements.

