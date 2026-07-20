# Cryptolens: Register Event

Creates an analytics event in Cryptolens.

```
POST https://connect.mindcloud.co/v1/universal/cryptolens/latest/actions/register-event
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cryptolens `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/cryptolens/latest/actions/register-event" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/cryptolens/latest/actions/register-event', {
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
| `currency` | string | no | Currency code for the event value. |
| `eventName` | string | no | Event name such as click or start. |
| `featureName` | string | no | Feature name associated with the event. |
| `key` | string | no | License key string. |
| `machineCode` | string | no | Machine code or device identifier. |
| `metadata` | string | no | Event metadata as a JSON string. |
| `productId` | string | no | Product ID. Required only when Key is also supplied. |
| `v` | string | no | Method version. |
| `value` | string | no | Integer event value; for example 2530 for 25.30. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string",
      "result": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string | Message returned by Register Event. |
| `result` | number | Result code returned by Register Event. |

## Native endpoint

Through the native Cryptolens API, this operation is `GET /api/ai/RegisterEvent` (base URL `https://api.cryptolens.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/register-event.md) for the provider-specific parameters and requirements.

