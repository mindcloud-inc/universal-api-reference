# Nango: Get Integration Functions Config



```
GET https://connect.mindcloud.co/v1/universal/nango/latest/actions/get-integration-functions-config
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Nango `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/nango/latest/actions/get-integration-functions-config?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/nango/latest/actions/get-integration-functions-config?${params}`, {
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
      "actions": [
        {}
      ],
      "providerConfigKey": "string",
      "syncs": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `actions` | array<object> |  |
| `providerConfigKey` | string |  |
| `syncs` | array<object> |  |

## Native endpoint

Through the native Nango API, this operation is `GET /scripts/config` (base URL `https://api.nango.dev`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-integration-functions-config.md) for the provider-specific parameters and requirements.

