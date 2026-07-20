# Skyfire: Introspect Token

Retrieves token details from Skyfire.

```
GET https://connect.mindcloud.co/v1/universal/skyfire/latest/actions/introspect-token
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Skyfire `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/skyfire/latest/actions/introspect-token?connectionId=$CONNECTION_ID&token=eyJhbGciOi..." \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "token": "eyJhbGciOi..."
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/skyfire/latest/actions/introspect-token?${params}`, {
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
| `token` | string | yes | The complete JWT string as issued to the buyer, not a tokenId. Can be of any token type: kya, pay, or kya-pay. Example: `eyJhbGciOi...`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "chargeableUntil": 1,
      "expiresAt": 1,
      "isValid": true,
      "remainingBalance": "string",
      "validationError": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `chargeableUntil` | number |  |
| `expiresAt` | number |  |
| `isValid` | boolean |  |
| `remainingBalance` | string |  |
| `validationError` | string |  |

## Native endpoint

Through the native Skyfire API, this operation is `POST /tokens/introspect` (base URL `https://api.skyfire.xyz/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/introspect-token.md) for the provider-specific parameters and requirements.

