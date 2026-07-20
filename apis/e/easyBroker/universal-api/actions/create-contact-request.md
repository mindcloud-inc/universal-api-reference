# EasyBroker: Create Contact Request

Creates or updates a property contact request in EasyBroker.

```
POST https://connect.mindcloud.co/v1/universal/easyBroker/latest/actions/create-contact-request
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a EasyBroker `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/easyBroker/latest/actions/create-contact-request" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "propertyId": "string",
  "name": "Ava Chen",
  "message": "string",
  "source": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/easyBroker/latest/actions/create-contact-request', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "propertyId": "string",
    "name": "Ava Chen",
    "message": "string",
    "source": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `propertyId` | string | yes | Property ID that received the contact request. |
| `name` | string | yes | Lead full name. |
| `email` | string | no | Lead email address. |
| `phone` | string | no | Lead phone number. |
| `message` | string | yes | Lead message. |
| `source` | string | yes | Contact source label. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native EasyBroker API returns.

## Native endpoint

Through the native EasyBroker API, this operation is `POST /contact_requests` (base URL `https://api.easybroker.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-contact-request.md) for the provider-specific parameters and requirements.

