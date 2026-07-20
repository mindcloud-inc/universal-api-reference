# Infobip: Create 2FA Application



```
POST https://connect.mindcloud.co/v1/universal/infobip/latest/actions/create2fa-application
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Infobip `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/infobip/latest/actions/create2fa-application" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/infobip/latest/actions/create2fa-application', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `configuration` | object | no |  |
| `configuration.allowMultiplePinVerifications` | boolean | no | Indicates whether multiple PIN verification is allowed. |
| `configuration.pinAttempts` | number | no | Number of possible PIN attempts. |
| `configuration.pinTimeToLive` | string | no | Validity period of PIN in specified time unit. Required format: `{timeLength}{timeUnit}`. `timeLength` is optional with a default value of 1. `timeUnit` can be set to: `ms`, `s`, `m`, `h` or `d` representing milliseconds, seconds, minutes, hours, and days respectively. Must not exceed one year, although much lower value is recommended. |
| `configuration.sendPinPerApplicationLimit` | string | no | Overall number of requests over a specified time period for generating a PIN and sending a message using a single application. Required format: `{attempts}/{timeLength}{timeUnit}`. `attempts` and `timeunit` are mandatory and `timeLength` is optional with a default value of 1. `timeUnit` is one of: `ms`, `s`, `m`, `h` or `d` representing milliseconds, seconds, minutes, hours, and days respectively. Must not exceed one year, although much lower value is recommended. |
| `configuration.sendPinPerPhoneNumberLimit` | string | no | Number of requests over a specified time period for generating a PIN and sending a message to one destination. Required format: `{attempts}/{timeLength}{timeUnit}`. `attempts` and `timeunit` are mandatory and `timeLength` is optional with a default value of 1. `timeUnit` is one of: `ms`, `s`, `m`, `h` or `d` representing milliseconds, seconds, minutes, hours, and days respectively. Must not exceed one year, although much lower value is recommended. |
| `configuration.verifyPinLimit` | string | no | The number of PIN verification requests over a specififed time period from one phone number (MSISDN). Required format: `{attempts}/{timeLength}{timeUnit}`. `attempts` and `timeunit` are mandatory and `timeLength` is optional with a default value of 1. `timeUnit` is one of: `ms`, `s`, `m`, `h` or `d` representing milliseconds, seconds, minutes, hours, and days respectively. Must not exceed one day, although much lower value is recommended. |
| `enabled` | boolean | no | Indicates whether the created application is enabled. |
| `name` | string | yes | 2FA application name. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "applicationId": "string",
      "configuration": {
        "allowMultiplePinVerifications": true,
        "pinAttempts": 1,
        "pinTimeToLive": "string",
        "sendPinPerApplicationLimit": "string",
        "sendPinPerPhoneNumberLimit": "string",
        "verifyPinLimit": "string"
      },
      "enabled": true,
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `applicationId` | string |  |
| `configuration` | object |  |
| `configuration.allowMultiplePinVerifications` | boolean |  |
| `configuration.pinAttempts` | number |  |
| `configuration.pinTimeToLive` | string |  |
| `configuration.sendPinPerApplicationLimit` | string |  |
| `configuration.sendPinPerPhoneNumberLimit` | string |  |
| `configuration.verifyPinLimit` | string |  |
| `enabled` | boolean |  |
| `name` | string |  |

## Native endpoint

Through the native Infobip API, this operation is `POST /2fa/2/applications` (base URL `https://rkpzwe.api.infobip.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create2fa-application.md) for the provider-specific parameters and requirements.

