# Feishu Document: Get Tenant Access Token

Retrieves a tenant access token from Feishu.

```
POST https://connect.mindcloud.co/v1/universal/feishuDocument/latest/actions/get-tenant-access-token
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Feishu Document `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/feishuDocument/latest/actions/get-tenant-access-token" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/feishuDocument/latest/actions/get-tenant-access-token', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
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
| `code` | number | Provider error code. Zero means success. |
| `expire` | number | Token lifetime in seconds. |
| `msg` | string | Provider status message. |
| `tenant_access_token` | string | Tenant access token returned for the custom app. |

## Native endpoint

Through the native Feishu Document API, this operation is `POST /open-apis/auth/v3/tenant_access_token/internal` (base URL `https://open.larksuite.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-tenant-access-token.md) for the provider-specific parameters and requirements.

