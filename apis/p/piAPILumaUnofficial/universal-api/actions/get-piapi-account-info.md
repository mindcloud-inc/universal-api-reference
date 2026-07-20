# PiAPI/Luma (unofficial): Get PiAPI Account Info

Retrieves connected account details from PiAPI.

```
GET https://connect.mindcloud.co/v1/universal/piAPILumaUnofficial/latest/actions/get-piapi-account-info
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PiAPI/Luma (unofficial) `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/piAPILumaUnofficial/latest/actions/get-piapi-account-info?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/piAPILumaUnofficial/latest/actions/get-piapi-account-info?${params}`, {
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
      "code": 1,
      "data": {
        "id": 1,
        "name": "Ava Chen",
        "plan": "string",
        "platform": "string",
        "type": "string",
        "wallet": {
          "luma_remain": 1
        }
      },
      "message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `code` | number | PiAPI status code. |
| `data` | object | PiAPI account payload. |
| `data.id` | number | Account identifier. |
| `data.name` | string | Account display name. |
| `data.plan` | string | Current PiAPI plan. |
| `data.platform` | string | Provider platform token. |
| `data.type` | string | Account billing type. |
| `data.wallet` | object | Wallet and credit balances. |
| `data.wallet.luma_remain` | number | Remaining Luma balance reported by PiAPI. |
| `message` | string | PiAPI status message. |

## Native endpoint

Through the native PiAPI/Luma (unofficial) API, this operation is `GET /account/info` (base URL `https://api.piapi.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-piapi-account-info.md) for the provider-specific parameters and requirements.

