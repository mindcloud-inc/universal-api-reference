# IdentityCheck: Create Direct Verification



```
POST https://connect.mindcloud.co/v1/universal/identityCheck/latest/actions/create-direct-verification
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a IdentityCheck `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/identityCheck/latest/actions/create-direct-verification" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "email": "ava@example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/identityCheck/latest/actions/create-direct-verification', {
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
| `contactId` | string | no | Optional upstream contact identifier. |
| `email` | string | yes | Email address for the verification invite. |
| `emailUser` | string | no | Whether IdentityCheck should email the user. |
| `firstName` | string | no | First name of the person to verify. |
| `lastName` | string | no | Last name of the person to verify. |
| `triggeredBy` | string | no | Source label for how the verification was triggered. Default: `direct`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accountName": "Ava Chen",
      "email": "ava@example.com",
      "firstName": "Ava",
      "id": "string",
      "lastName": "Chen",
      "triggeredBy": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accountName` | string | IdentityCheck account name associated with the created verification. |
| `email` | string | Email used for the verification invite. |
| `firstName` | string | First name on the created verification. |
| `id` | string | IdentityCheck verification identifier. |
| `lastName` | string | Last name on the created verification. |
| `triggeredBy` | string | Source label for how the verification was triggered. |
| `type` | string | Verification type returned by IdentityCheck. |

## Native endpoint

Through the native IdentityCheck API, this operation is `POST /direct-verification` (base URL `https://identity.stackgo.io/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-direct-verification.md) for the provider-specific parameters and requirements.

