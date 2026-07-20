# PiAPI/FaceSwap: Get Account Info

Retrieves account details from PiAPI/FaceSwap.

```
GET https://connect.mindcloud.co/v1/universal/piAPIFaceSwap/latest/actions/get-account-info
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PiAPI/FaceSwap `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/piAPIFaceSwap/latest/actions/get-account-info?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/piAPIFaceSwap/latest/actions/get-account-info?${params}`, {
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
        "max_concurrent_task_count": 1,
        "name": "Ava Chen",
        "plan": "string",
        "platform": "string",
        "type": "string",
        "wallet": {}
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
| `code` | number | PiAPI response code. |
| `data` | object | PiAPI account information payload. |
| `data.id` | number | PiAPI account identifier. |
| `data.max_concurrent_task_count` | number | Maximum concurrent task count. |
| `data.name` | string | PiAPI account name or email. |
| `data.plan` | string | Current PiAPI plan. |
| `data.platform` | string | Provider platform name. |
| `data.type` | string | Account billing type. |
| `data.wallet` | object | Wallet and balance information. |
| `message` | string | PiAPI response message. |

## Native endpoint

Through the native PiAPI/FaceSwap API, this operation is `GET /account/info` (base URL `https://api.piapi.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-account-info.md) for the provider-specific parameters and requirements.

