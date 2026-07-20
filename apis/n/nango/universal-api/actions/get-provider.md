# Nango: Get Provider



```
GET https://connect.mindcloud.co/v1/universal/nango/latest/actions/get-provider
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Nango `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/nango/latest/actions/get-provider?connectionId=$CONNECTION_ID&provider=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "provider": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/nango/latest/actions/get-provider?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `provider` | string | yes | Provider slug to retrieve. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "authMode": "string",
      "key": "string",
      "name": "Ava Chen",
      "proxyBaseUrl": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `authMode` | string |  |
| `key` | string |  |
| `name` | string |  |
| `proxyBaseUrl` | string |  |

## Native endpoint

Through the native Nango API, this operation is `GET /providers/:provider` (base URL `https://api.nango.dev`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-provider.md) for the provider-specific parameters and requirements.

