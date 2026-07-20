# Globalping: List Probes

Retrieves available Globalping probes.

```
GET https://connect.mindcloud.co/v1/universal/globalping/latest/actions/list-probes
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Globalping `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/globalping/latest/actions/list-probes?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/globalping/latest/actions/list-probes?${params}`, {
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
      "location": {},
      "resolvers": [
        "string"
      ],
      "tags": [
        "string"
      ],
      "version": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `location` | object | Probe geographic and network location details. |
| `resolvers` | array<string> | DNS resolvers configured on the probe. |
| `tags` | array<string> | Probe classification and user tags. |
| `version` | string | Probe software version. |

## Native endpoint

Through the native Globalping API, this operation is `GET /v1/probes` (base URL `https://api.globalping.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-probes.md) for the provider-specific parameters and requirements.

