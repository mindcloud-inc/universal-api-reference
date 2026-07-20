# Ascora: Update Quote Status

Updates the status of a quote in Ascora.

```
PUT https://connect.mindcloud.co/v1/universal/ascora/latest/actions/update-quote-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ascora `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/ascora/latest/actions/update-quote-status" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/ascora/latest/actions/update-quote-status', {
  method: 'PUT',
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
| `quoteNumber` | string | no |  |
| `quoteStatus` | string | no | IN-PROGRESS, SENT-TO-CUSTOMER, LOST, or WON. |
| `reasonForLoss` | string | no | Applied when the quote status is LOST. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string",
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string | Ascora status update result message. |
| `success` | boolean | Whether Ascora updated the quote status. |

## Native endpoint

Through the native Ascora API, this operation is `POST /Quotes/UpdateStatus` (base URL `https://api.ascora.com.au`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-quote-status.md) for the provider-specific parameters and requirements.

