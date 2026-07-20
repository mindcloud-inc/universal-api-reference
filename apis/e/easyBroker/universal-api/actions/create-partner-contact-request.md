# EasyBroker: Create Partner Contact Request

Creates a partner contact request in EasyBroker.

```
POST https://connect.mindcloud.co/v1/universal/easyBroker/latest/actions/create-partner-contact-request
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a EasyBroker `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/easyBroker/latest/actions/create-partner-contact-request" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "message": "string",
  "propertyId": "string",
  "remoteId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/easyBroker/latest/actions/create-partner-contact-request', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "message": "string",
    "propertyId": "string",
    "remoteId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `email` | string | no | Requester email. Required if phone is not present. |
| `message` | string | yes | Message of the contact request. |
| `name` | string | no | Requester name. |
| `phone` | string | no | Requester phone number. Required if email is not present. |
| `propertyId` | string | yes | The EasyBroker property id related to the contact request. |
| `remoteId` | number | yes | A unique numeric id of the contact request from your website. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native EasyBroker API returns.

## Native endpoint

Through the native EasyBroker API, this operation is `POST /integration_partners/contact_requests` (base URL `https://api.easybroker.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-partner-contact-request.md) for the provider-specific parameters and requirements.

