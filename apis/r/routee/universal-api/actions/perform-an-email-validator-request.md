# Routee: Perform an Email Validator request

Creates an email validator request in Routee.

```
POST https://connect.mindcloud.co/v1/universal/routee/latest/actions/perform-an-email-validator-request
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Routee `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/routee/latest/actions/perform-an-email-validator-request" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "email": "ava@example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/routee/latest/actions/perform-an-email-validator-request', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "email": "ava@example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `email` | string | yes | This is the email address to perform the validation. |
| `label` | string | no | This is the label that will be given to tag a specific Email Validation request. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "string",
      "details": {
        "exists": true,
        "hasValidDNS": true,
        "hasValidFormat": true
      },
      "email": "ava@example.com",
      "label": "string",
      "price": 1,
      "trackingId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | string |  |
| `details` | object |  |
| `details.exists` | boolean |  |
| `details.hasValidDNS` | boolean |  |
| `details.hasValidFormat` | boolean |  |
| `email` | string |  |
| `label` | string |  |
| `price` | number |  |
| `trackingId` | string |  |

## Native endpoint

Through the native Routee API, this operation is `POST /emailvalidator` (base URL `https://connect.routee.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/perform-an-email-validator-request.md) for the provider-specific parameters and requirements.

