# Element: Get Capabilities

Retrieves supported capabilities from Element.

```
GET https://connect.mindcloud.co/v1/universal/element/latest/actions/get-capabilities
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Element `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/element/latest/actions/get-capabilities?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/element/latest/actions/get-capabilities?${params}`, {
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
      "capabilities": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `capabilities` | object |  |

## Native endpoint

Through the native Element API, this operation is `GET /_matrix/client/v3/capabilities` (base URL `{{credentials.homeserverUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-capabilities.md) for the provider-specific parameters and requirements.

