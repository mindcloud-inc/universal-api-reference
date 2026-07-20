# Omnisend: Trigger Custom Event

Triggers a custom event in Omnisend.

```
POST https://connect.mindcloud.co/v1/universal/omnisend/latest/actions/trigger-custom-event
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Omnisend `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/omnisend/latest/actions/trigger-custom-event" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "contact": {},
  "eventName": "Ava Chen",
  "origin": "api"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/omnisend/latest/actions/trigger-custom-event', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "contact": {},
    "eventName": "Ava Chen",
    "origin": "api"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `contact` | object | yes |  |
| `contact.address` | string | no |  |
| `contact.birthdate` | date | no |  |
| `contact.city` | string | no |  |
| `contact.country` | string | no |  |
| `contact.customProperties` | object | no |  |
| `contact.email` | string | no |  |
| `contact.firstName` | string | no |  |
| `contact.gender` | string | no |  |
| `contact.id` | string | no |  |
| `contact.lastName` | string | no |  |
| `contact.phone` | string | no |  |
| `contact.postalCode` | string | no |  |
| `contact.state` | string | no |  |
| `contact.tags[]` | array<string> | no |  |
| `eventID` | string | no |  |
| `eventName` | string | yes |  |
| `eventVersion` | string | no |  |
| `origin` | string | yes | Default: `api`. |
| `properties` | object | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Omnisend API returns.

## Native endpoint

Through the native Omnisend API, this operation is `POST /v5/events` (base URL `https://api.omnisend.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/trigger-custom-event.md) for the provider-specific parameters and requirements.

