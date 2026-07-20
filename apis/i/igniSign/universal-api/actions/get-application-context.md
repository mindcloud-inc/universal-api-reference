# IgniSign: Get Application Context



```
GET https://connect.mindcloud.co/v1/universal/igniSign/latest/actions/get-application-context
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a IgniSign `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/igniSign/latest/actions/get-application-context?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/igniSign/latest/actions/get-application-context?${params}`, {
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
      "_createdAt": "string",
      "appId": "string",
      "appName": "Ava Chen",
      "appType": "string",
      "config": {},
      "envSettings": {},
      "ignisignApiVersion": "string",
      "orgId": "string",
      "settings": {},
      "signatureProfiles": {},
      "signerProfiles": {},
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `_createdAt` | string |  |
| `appId` | string |  |
| `appName` | string |  |
| `appType` | string |  |
| `config` | object |  |
| `envSettings` | object |  |
| `ignisignApiVersion` | string |  |
| `orgId` | string |  |
| `settings` | object |  |
| `signatureProfiles` | object |  |
| `signerProfiles` | object |  |
| `status` | string |  |

## Native endpoint

Through the native IgniSign API, this operation is `GET /v4/applications/:appId/context` (base URL `https://api.ignisign.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-application-context.md) for the provider-specific parameters and requirements.

