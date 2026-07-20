# Cloutly: Send Review Invite

Creates a customer review invite in Cloutly.

```
POST https://connect.mindcloud.co/v1/universal/cloutly/latest/actions/send-review-invite
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cloutly `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/cloutly/latest/actions/send-review-invite" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "businessId": "string",
  "firstName": "Ava",
  "lastName": "Chen",
  "email": "ava@example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/cloutly/latest/actions/send-review-invite', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "businessId": "string",
    "firstName": "Ava",
    "lastName": "Chen",
    "email": "ava@example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `businessId` | string | yes | Business to send the review invite from. |
| `firstName` | string | yes | Customer first name. |
| `lastName` | string | yes | Customer last name. |
| `email` | string | yes | Customer email address. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "contact": {},
      "usage": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `contact` | object | Contact created or updated for the invite. |
| `usage` | object | Usage metadata returned by Cloutly. |

## Native endpoint

Through the native Cloutly API, this operation is `POST /send-review-invite` (base URL `https://app.cloutly.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-review-invite.md) for the provider-specific parameters and requirements.

