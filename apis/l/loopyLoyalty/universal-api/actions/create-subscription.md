# Loopy Loyalty: Create Subscription



```
POST https://connect.mindcloud.co/v1/universal/loopyLoyalty/latest/actions/create-subscription
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Loopy Loyalty `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/loopyLoyalty/latest/actions/create-subscription" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "url": "https://example.com",
  "event": "string",
  "cardId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/loopyLoyalty/latest/actions/create-subscription', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "url": "https://example.com",
    "event": "string",
    "cardId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `url` | string | yes | Target URL to POST the event data to. |
| `event` | string | yes | Event type that triggers the POST. |
| `cardId` | string | yes | Campaign ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string | Created subscription ID. |

## Native endpoint

Through the native Loopy Loyalty API, this operation is `POST /subscription` (base URL `https://api.loopyloyalty.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-subscription.md) for the provider-specific parameters and requirements.

