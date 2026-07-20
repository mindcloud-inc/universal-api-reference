# Lark Drive: Get Tenant Access Token



```
POST https://connect.mindcloud.co/v1/universal/larkDrive/latest/actions/get-tenant-access-token
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Lark Drive `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/larkDrive/latest/actions/get-tenant-access-token" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/larkDrive/latest/actions/get-tenant-access-token', {
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
| `code` | number |  |
| `expire` | number |  |
| `msg` | string |  |
| `tenant_access_token` | string |  |

## Native endpoint

Through the native Lark Drive API, this operation is `POST /auth/v3/tenant_access_token/internal` (base URL `https://open.larksuite.com/open-apis`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-tenant-access-token.md) for the provider-specific parameters and requirements.

