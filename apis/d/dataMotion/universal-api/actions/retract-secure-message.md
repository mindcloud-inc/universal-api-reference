# DataMotion: Retract Secure Message

Retracts a previously sent secure message in DataMotion.

```
DELETE https://connect.mindcloud.co/v1/universal/dataMotion/latest/actions/retract-secure-message
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DataMotion `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/dataMotion/latest/actions/retract-secure-message?connectionId=$CONNECTION_ID&transactionId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "transactionId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dataMotion/latest/actions/retract-secure-message?${params}`, {
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
| `transactionId` | string | yes | Transaction ID of the secure message to retract. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `success` | boolean | True when DataMotion accepts the retraction request. |

## Native endpoint

Through the native DataMotion API, this operation is `DELETE /v1.2/:transactionId/Retract` (base URL `https://api.datamotion.com/SecureMessageDelivery`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retract-secure-message.md) for the provider-specific parameters and requirements.

