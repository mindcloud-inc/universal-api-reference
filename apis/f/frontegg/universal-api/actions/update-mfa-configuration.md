# Frontegg: Update MFA Configuration

Updates MFA configuration for your Frontegg environment.

```
PUT https://connect.mindcloud.co/v1/universal/frontegg/latest/actions/update-mfa-configuration
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Frontegg `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/frontegg/latest/actions/update-mfa-configuration" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "authenticationApp.active": true,
  "authenticationApp.serviceName": "Ava Chen",
  "sms.active": true,
  "sms.tokenLifetimeSeconds": 1,
  "email.active": true,
  "email.tokenLifetimeSeconds": 1,
  "email.sender": "ava@example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/frontegg/latest/actions/update-mfa-configuration', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "authenticationApp.active": true,
    "authenticationApp.serviceName": "Ava Chen",
    "sms.active": true,
    "sms.tokenLifetimeSeconds": 1,
    "email.active": true,
    "email.tokenLifetimeSeconds": 1,
    "email.sender": "ava@example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `authenticationApp.active` | boolean | yes | Whether authenticator app MFA is active. |
| `authenticationApp.serviceName` | string | yes | Authenticator app service name. |
| `sms.active` | boolean | yes | Whether SMS MFA is active. |
| `sms.tokenLifetimeSeconds` | number | yes | SMS MFA token lifetime in seconds. |
| `email.active` | boolean | yes | Whether email MFA is active. |
| `email.tokenLifetimeSeconds` | number | yes | Email MFA token lifetime in seconds. |
| `email.sender` | string | yes | Email MFA sender address. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "authenticationApp": {
        "active": true,
        "serviceName": "Ava Chen"
      },
      "email": {
        "active": true,
        "sender": "ava@example.com",
        "tokenLifetimeSeconds": 1
      },
      "sms": {
        "active": true,
        "tokenLifetimeSeconds": 1
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `authenticationApp.active` | boolean |  |
| `authenticationApp.serviceName` | string |  |
| `email.active` | boolean |  |
| `email.sender` | string |  |
| `email.tokenLifetimeSeconds` | number |  |
| `sms.active` | boolean |  |
| `sms.tokenLifetimeSeconds` | number |  |

## Native endpoint

Through the native Frontegg API, this operation is `POST /identity/resources/configurations/v1/mfa` (base URL `https://api.frontegg.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-mfa-configuration.md) for the provider-specific parameters and requirements.

