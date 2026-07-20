# PiAPI/Hunyuan: Get Account Info



```
GET https://connect.mindcloud.co/v1/universal/piAPIHunyuan/latest/actions/get-account-info
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PiAPI/Hunyuan `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/piAPIHunyuan/latest/actions/get-account-info?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/piAPIHunyuan/latest/actions/get-account-info?${params}`, {
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
      "accountGroup": "string",
      "accountMjBotGroupRelations": [
        {}
      ],
      "accountMjWorkerNodeGroupRelations": [
        {}
      ],
      "accountTags": [
        {}
      ],
      "createdAt": "2026-05-07T12:00:00.000Z",
      "creditPackInfo": {},
      "deletedAt": "2026-05-07T12:00:00.000Z",
      "equivalentInUsd": 1,
      "id": 1,
      "isEnable": true,
      "isUsingPrivateChatGptPool": true,
      "isUsingPrivateKlingPool": true,
      "isUsingPrivateLumaPool": true,
      "isUsingPrivateSunoPool": true,
      "isUsingPrivateUdioPool": true,
      "isVerified": true,
      "klingFailoverEnabled": true,
      "lumaFailoverEnabled": true,
      "maxConcurrentTaskCount": 1,
      "mjFailoverEnabled": true,
      "name": "Ava Chen",
      "notificationHookUrl": "https://example.com",
      "plan": "string",
      "platform": "string",
      "privatePoolSize": 1,
      "sunoFailoverEnabled": true,
      "type": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "wallet": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accountGroup` | string |  |
| `accountMjBotGroupRelations` | array<object> |  |
| `accountMjWorkerNodeGroupRelations` | array<object> |  |
| `accountTags` | array<object> |  |
| `createdAt` | date |  |
| `creditPackInfo` | object | Credit pack summary details |
| `deletedAt` | date |  |
| `equivalentInUsd` | number |  |
| `id` | number | PiAPI account ID |
| `isEnable` | boolean | Whether the account is enabled |
| `isUsingPrivateChatGptPool` | boolean |  |
| `isUsingPrivateKlingPool` | boolean |  |
| `isUsingPrivateLumaPool` | boolean |  |
| `isUsingPrivateSunoPool` | boolean |  |
| `isUsingPrivateUdioPool` | boolean |  |
| `isVerified` | boolean |  |
| `klingFailoverEnabled` | boolean |  |
| `lumaFailoverEnabled` | boolean |  |
| `maxConcurrentTaskCount` | number |  |
| `mjFailoverEnabled` | boolean |  |
| `name` | string | Account display name or email |
| `notificationHookUrl` | string |  |
| `plan` | string |  |
| `platform` | string |  |
| `privatePoolSize` | number |  |
| `sunoFailoverEnabled` | boolean |  |
| `type` | string |  |
| `updatedAt` | date |  |
| `wallet` | object | Wallet balances and usage details |

## Native endpoint

Through the native PiAPI/Hunyuan API, this operation is `GET /account/info` (base URL `https://api.piapi.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-account-info.md) for the provider-specific parameters and requirements.

