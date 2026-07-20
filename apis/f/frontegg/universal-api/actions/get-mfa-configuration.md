# Frontegg: Get MFA Configuration

Retrieves MFA configuration for your Frontegg environment.

```
GET https://connect.mindcloud.co/v1/universal/frontegg/latest/actions/get-mfa-configuration
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Frontegg `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/frontegg/latest/actions/get-mfa-configuration?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/frontegg/latest/actions/get-mfa-configuration?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



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

Through the native Frontegg API, this operation is `GET /identity/resources/configurations/v1/mfa` (base URL `https://api.frontegg.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-mfa-configuration.md) for the provider-specific parameters and requirements.

