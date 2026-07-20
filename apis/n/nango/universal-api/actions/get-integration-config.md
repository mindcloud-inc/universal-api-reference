# Nango: Get Integration (Config)



```
GET https://connect.mindcloud.co/v1/universal/nango/latest/actions/get-integration-config
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Nango `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/nango/latest/actions/get-integration-config?connectionId=$CONNECTION_ID&providerConfigKey=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "providerConfigKey": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/nango/latest/actions/get-integration-config?${params}`, {
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
| `providerConfigKey` | string | yes | The provider configuration key for the integration. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "config": {},
      "properties": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `config` | object |  |
| `properties` | object |  |

## Native endpoint

Through the native Nango API, this operation is `GET /config/:providerConfigKey` (base URL `https://api.nango.dev`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-integration-config.md) for the provider-specific parameters and requirements.

