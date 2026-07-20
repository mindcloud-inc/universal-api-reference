# Fingertip: Create Site Contact



```
POST https://connect.mindcloud.co/v1/universal/fingertip/latest/actions/create-site-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Fingertip `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/fingertip/latest/actions/create-site-contact" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "email": "ava@example.com",
  "siteId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/fingertip/latest/actions/create-site-contact', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "email": "ava@example.com",
    "siteId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `email` | string | yes | Contact email address. |
| `siteId` | string | yes | Site ID. |
| `firstName` | string | no | Contact first name. |
| `lastName` | string | no | Contact last name. |
| `phone` | string | no | Contact phone number. |
| `notes` | string | no | Internal notes. |
| `marketingStatus` | string | no | Optional marketing status. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Fingertip API returns.

## Native endpoint

Through the native Fingertip API, this operation is `POST /v1/site-contacts` (base URL `https://api.fingertip.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-site-contact.md) for the provider-specific parameters and requirements.

