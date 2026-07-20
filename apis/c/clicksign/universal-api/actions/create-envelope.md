# Clicksign: Create Envelope

Creates an envelope in Clicksign.

```
POST https://connect.mindcloud.co/v1/universal/clicksign/latest/actions/create-envelope
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Clicksign `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/clicksign/latest/actions/create-envelope" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "data.attributes.name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/clicksign/latest/actions/create-envelope', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "data.attributes.name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `data` | object | no | JSON:API document wrapper. |
| `data.attributes` | object | no | Envelope attributes. |
| `data.attributes.autoClose` | boolean | no | Whether the envelope closes automatically. |
| `data.attributes.blockAfterRefusal` | boolean | no | Whether the envelope blocks after refusal. |
| `data.attributes.deadlineAt` | date | no | The signing deadline timestamp. |
| `data.attributes.defaultMessage` | string | no | Default notification message. |
| `data.attributes.defaultSubject` | string | no | Default notification subject. |
| `data.attributes.locale` | string | no | The envelope locale. |
| `data.attributes.name` | string | yes | The envelope name. |
| `data.attributes.remindInterval` | number | no | Reminder interval in days. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Clicksign API returns.

## Native endpoint

Through the native Clicksign API, this operation is `POST /envelopes` (base URL `https://app.clicksign.com/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-envelope.md) for the provider-specific parameters and requirements.

