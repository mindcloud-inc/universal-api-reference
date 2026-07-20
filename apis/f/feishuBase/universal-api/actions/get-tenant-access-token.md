# Feishu Base: Get Tenant Access Token

Retrieves a Feishu tenant access token.

```
GET https://connect.mindcloud.co/v1/universal/feishuBase/latest/actions/get-tenant-access-token
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Feishu Base `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/feishuBase/latest/actions/get-tenant-access-token?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/feishuBase/latest/actions/get-tenant-access-token?${params}`, {
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
      "expire": 1,
      "msg": "string",
      "tenant_access_token": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `code` | number |  |
| `expire` | number |  |
| `msg` | string |  |
| `tenant_access_token` | string |  |

## Native endpoint

Through the native Feishu Base API, this operation is `POST https://open.feishu.cn/open-apis/auth/v3/tenant_access_token/internal` (base URL `https://open.feishu.cn/open-apis/bitable/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-tenant-access-token.md) for the provider-specific parameters and requirements.

