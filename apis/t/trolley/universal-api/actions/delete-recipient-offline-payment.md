# Trolley: Delete Recipient Offline Payment

Deletes a recipient offline payment from Trolley.

```
DELETE https://connect.mindcloud.co/v1/universal/trolley/latest/actions/delete-recipient-offline-payment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Trolley `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/trolley/latest/actions/delete-recipient-offline-payment?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/trolley/latest/actions/delete-recipient-offline-payment?${params}`, {
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
| `offlinePaymentId` | string | no | Offline payment ID |
| `recipientId` | string | no | Recipient ID |

## Response

```json
{
  "success": true,
  "data": [
    {
      "ok": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `ok` | boolean |  |

## Native endpoint

Through the native Trolley API, this operation is `DELETE /v1/recipients/:recipientId/offlinePayments/:offlinePaymentId` (base URL `https://api.trolley.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-recipient-offline-payment.md) for the provider-specific parameters and requirements.

