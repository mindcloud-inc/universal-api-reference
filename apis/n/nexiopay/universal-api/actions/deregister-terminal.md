# Nexiopay: Deregister terminal



```
DELETE https://connect.mindcloud.co/v1/universal/nexiopay/latest/actions/deregister-terminal
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Nexiopay `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/nexiopay/latest/actions/deregister-terminal?connectionId=$CONNECTION_ID&terminalId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "terminalId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/nexiopay/latest/actions/deregister-terminal?${params}`, {
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
| `terminalId` | string | yes | Nexio terminal ID to deregister. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string",
      "status": "string",
      "terminalId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string | Nexio response message. |
| `status` | string | Deregistration status. |
| `terminalId` | string | Encoded Nexio terminal ID. |

## Native endpoint

Through the native Nexiopay API, this operation is `POST /pay/v3/deregisterTerminal` (base URL `https://api.nexiopaysandbox.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/deregister-terminal.md) for the provider-specific parameters and requirements.

