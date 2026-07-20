# Infobip: Get 2FA Applications



```
GET https://connect.mindcloud.co/v1/universal/infobip/latest/actions/get2fa-applications
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Infobip `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/infobip/latest/actions/get2fa-applications?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/infobip/latest/actions/get2fa-applications?${params}`, {
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

Through the native Infobip API, this operation is `GET /2fa/2/applications` (base URL `https://rkpzwe.api.infobip.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get2fa-applications.md) for the provider-specific parameters and requirements.

