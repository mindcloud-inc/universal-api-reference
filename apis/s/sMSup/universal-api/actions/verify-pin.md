# SMSup: Verify PIN



```
GET https://connect.mindcloud.co/v1/universal/sMSup/latest/actions/verify-pin
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SMSup `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sMSup/latest/actions/verify-pin?connectionId=$CONNECTION_ID&msisdn=34666666111&pin=581365" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "msisdn": "34666666111",
  "pin": "581365"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sMSup/latest/actions/verify-pin?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `msisdn` | string | yes | Mobile number that previously requested verification. Example: `34666666111`. |
| `pin` | string | yes | Verification PIN received by the user. Example: `581365`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string",
      "previouslyVerified": true,
      "triesRemaining": 1,
      "verified": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string |  |
| `previouslyVerified` | boolean |  |
| `triesRemaining` | number |  |
| `verified` | boolean |  |

## Native endpoint

Through the native SMSup API, this operation is `POST /api/2fa/verify` (base URL `https://api.gateway360.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/verify-pin.md) for the provider-specific parameters and requirements.

