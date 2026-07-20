# Nexiopay: View terminal list



```
GET https://connect.mindcloud.co/v1/universal/nexiopay/latest/actions/view-terminal-list
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Nexiopay `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/nexiopay/latest/actions/view-terminal-list?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/nexiopay/latest/actions/view-terminal-list?${params}`, {
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
      "deviceId": "string",
      "gatewayLabel": "string",
      "gatewayName": "Ava Chen",
      "gatewayType": 1,
      "merchantId": "string",
      "merchantName": "Ava Chen",
      "terminalId": "string",
      "terminalKey": "string",
      "terminalName": "Ava Chen",
      "terminalSerialNumber": "string",
      "terminalStatus": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `deviceId` | string | Terminal device ID. |
| `gatewayLabel` | string | Gateway label. |
| `gatewayName` | string | Payment gateway name. |
| `gatewayType` | number | Nexio gateway type identifier. |
| `merchantId` | string | Nexio merchant ID associated with the terminal. |
| `merchantName` | string | Merchant display name. |
| `terminalId` | string | Encoded Nexio terminal ID. |
| `terminalKey` | string | Terminal key when returned by Nexio. |
| `terminalName` | string | Terminal display name. |
| `terminalSerialNumber` | string | Terminal serial number. |
| `terminalStatus` | string | Terminal connection status. |

## Native endpoint

Through the native Nexiopay API, this operation is `GET /pay/v3/getTerminalList` (base URL `https://api.nexiopaysandbox.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/view-terminal-list.md) for the provider-specific parameters and requirements.

