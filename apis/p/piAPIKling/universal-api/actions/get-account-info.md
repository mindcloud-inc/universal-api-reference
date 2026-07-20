# PiAPI/Kling: Get Account Info



```
GET https://connect.mindcloud.co/v1/universal/piAPIKling/latest/actions/get-account-info
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PiAPI/Kling `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/piAPIKling/latest/actions/get-account-info?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/piAPIKling/latest/actions/get-account-info?${params}`, {
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
        "string"
      ],
      "createdAt": "string",
      "creditPackInfo": {},
      "equivalentInUsd": 1,
      "id": 1,
      "isEnable": true,
      "isVerified": true,
      "klingFailoverEnabled": true,
      "lumaFailoverEnabled": true,
      "maxConcurrentTaskCount": 1,
      "mjFailoverEnabled": true,
      "name": "Ava Chen",
      "notificationHookUrl": "https://example.com",
      "plan": "string",
      "platform": "string",
      "sunoFailoverEnabled": true,
      "type": "string",
      "updatedAt": "string",
      "wallet": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accountGroup` | string | Account group classification. |
| `accountMjBotGroupRelations` | array<object> | Midjourney bot group relations. |
| `accountMjWorkerNodeGroupRelations` | array<object> | Midjourney worker node group relations. |
| `accountTags` | array | Account tags. |
| `createdAt` | string | Account creation timestamp. |
| `creditPackInfo` | object | Credit pack summary information. |
| `equivalentInUsd` | number | Credit balance equivalent in USD. |
| `id` | number | PiAPI account ID. |
| `isEnable` | boolean | Whether the account is enabled. |
| `isVerified` | boolean | Whether the account is verified. |
| `klingFailoverEnabled` | boolean | Whether Kling failover is enabled. |
| `lumaFailoverEnabled` | boolean | Whether Luma failover is enabled. |
| `maxConcurrentTaskCount` | number | Maximum concurrent task count. |
| `mjFailoverEnabled` | boolean | Whether Midjourney failover is enabled. |
| `name` | string | Account display name or email. |
| `notificationHookUrl` | string | Configured notification webhook URL. |
| `plan` | string | Current PiAPI plan. |
| `platform` | string | Provider platform name. |
| `sunoFailoverEnabled` | boolean | Whether Suno failover is enabled. |
| `type` | string | Billing type. |
| `updatedAt` | string | Account update timestamp. |
| `wallet` | object | Wallet balances and credit usage details. |

## Native endpoint

Through the native PiAPI/Kling API, this operation is `GET /account/info` (base URL `https://api.piapi.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-account-info.md) for the provider-specific parameters and requirements.

