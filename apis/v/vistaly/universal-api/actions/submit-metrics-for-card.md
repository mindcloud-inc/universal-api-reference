# Vistaly: Submit Metrics for Card

Creates metrics for a card in Vistaly.

```
POST https://connect.mindcloud.co/v1/universal/vistaly/latest/actions/submit-metrics-for-card
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Vistaly `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/vistaly/latest/actions/submit-metrics-for-card" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "cardId": "string",
  "value": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/vistaly/latest/actions/submit-metrics-for-card', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "cardId": "string",
    "value": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `cardId` | string | yes | The unique identifier for the card whose metrics are being submitted. |
| `value` | number | yes | The metric value. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `timestamp` | date | no | The metric timestamp. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Vistaly API returns.

## Native endpoint

Through the native Vistaly API, this operation is `POST /v1/cards/{cardId}/metrics` (base URL `https://api.vistaly.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/submit-metrics-for-card.md) for the provider-specific parameters and requirements.

