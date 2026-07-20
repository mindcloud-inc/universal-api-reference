# Nango: Get Connection With Credentials (Deprecated)



```
GET https://connect.mindcloud.co/v1/universal/nango/latest/actions/get-connection-deprecated
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Nango `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/nango/latest/actions/get-connection-deprecated?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/nango/latest/actions/get-connection-deprecated?${params}`, {
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
      "connectionId": "string",
      "credentials": {},
      "provider": "string",
      "providerConfigKey": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `connectionId` | string |  |
| `credentials` | object |  |
| `provider` | string |  |
| `providerConfigKey` | string |  |

## Native endpoint

Through the native Nango API, this operation is `GET /connection/:connectionId` (base URL `https://api.nango.dev`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-connection-deprecated.md) for the provider-specific parameters and requirements.

