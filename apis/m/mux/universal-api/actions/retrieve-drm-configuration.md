# Mux: Retrieve DRM Configuration



```
GET https://connect.mindcloud.co/v1/universal/mux/latest/actions/retrieve-drm-configuration
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mux `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mux/latest/actions/retrieve-drm-configuration?connectionId=$CONNECTION_ID&drmConfigurationId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "drmConfigurationId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mux/latest/actions/retrieve-drm-configuration?${params}`, {
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
| `drmConfigurationId` | string | yes | The DRM configuration ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object |  |

## Native endpoint

Through the native Mux API, this operation is `GET /video/v1/drm-configurations/{DRM_CONFIGURATION_ID}` (base URL `https://api.mux.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-drm-configuration.md) for the provider-specific parameters and requirements.

