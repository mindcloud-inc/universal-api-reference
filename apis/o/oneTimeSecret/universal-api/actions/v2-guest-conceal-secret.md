# One-Time Secret: Guest Conceal Secret

Creates a guest secret from provided content in One-Time Secret.

```
POST https://connect.mindcloud.co/v1/universal/oneTimeSecret/latest/actions/v2-guest-conceal-secret
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a One-Time Secret `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/oneTimeSecret/latest/actions/v2-guest-conceal-secret" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "secret.shareDomain": "us.onetimesecret.com",
  "secret.secret": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/oneTimeSecret/latest/actions/v2-guest-conceal-secret', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "secret.shareDomain": "us.onetimesecret.com",
    "secret.secret": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `secret.shareDomain` | string | yes | Domain used for generated share URLs. Default: `us.onetimesecret.com`. |
| `secret.secret` | string | yes | The secret text to conceal. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "details": {},
      "record": {},
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `details` | object | Guest creation details returned by One-Time Secret. |
| `record` | object | Created guest secret, receipt, and metadata envelope. |
| `success` | boolean | Whether the guest secret was created. |

## Native endpoint

Through the native One-Time Secret API, this operation is `POST /api/v2/guest/secret/conceal` (base URL `https://us.onetimesecret.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/v2-guest-conceal-secret.md) for the provider-specific parameters and requirements.

