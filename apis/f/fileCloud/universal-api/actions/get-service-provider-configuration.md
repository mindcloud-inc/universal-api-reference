# FileCloud: Get Service Provider Configuration

Retrieves service provider configuration from FileCloud.

```
GET https://connect.mindcloud.co/v1/universal/fileCloud/latest/actions/get-service-provider-configuration
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a FileCloud `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fileCloud/latest/actions/get-service-provider-configuration?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fileCloud/latest/actions/get-service-provider-configuration?${params}`, {
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
      "authenticationSchemes": [
        {}
      ],
      "bulk": {},
      "changePassword": {},
      "etag": {},
      "filter": {},
      "meta": {},
      "patch": {},
      "schemas": [
        "string"
      ],
      "sort": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `authenticationSchemes` | array<object> |  |
| `bulk` | object |  |
| `changePassword` | object |  |
| `etag` | object |  |
| `filter` | object |  |
| `meta` | object |  |
| `patch` | object |  |
| `schemas` | array<string> |  |
| `sort` | object |  |

## Native endpoint

Through the native FileCloud API, this operation is `GET /scim/ServiceProviderConfig` (base URL `https://mindcloud.filecloudtrial.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-service-provider-configuration.md) for the provider-specific parameters and requirements.

