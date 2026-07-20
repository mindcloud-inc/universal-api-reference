# Nexiopay: Register terminal



```
POST https://connect.mindcloud.co/v1/universal/nexiopay/latest/actions/register-terminal
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Nexiopay `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/nexiopay/latest/actions/register-terminal" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "merchantId": "string",
  "terminalRegistrationCode": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/nexiopay/latest/actions/register-terminal', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "merchantId": "string",
    "terminalRegistrationCode": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `merchantId` | string | yes | Nexio merchant ID to associate with the terminal. |
| `terminalRegistrationCode` | string | yes | Registration code shown by the terminal. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "merchantId": "string",
      "status": "string",
      "terminalId": "string",
      "terminalName": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `merchantId` | string | Nexio merchant ID. |
| `status` | string | Registration status. |
| `terminalId` | string | Encoded Nexio terminal ID. |
| `terminalName` | string | Terminal display name. |

## Native endpoint

Through the native Nexiopay API, this operation is `POST /pay/v3/registerTerminal` (base URL `https://api.nexiopaysandbox.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/register-terminal.md) for the provider-specific parameters and requirements.

