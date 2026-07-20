# Tophhie Cloud: Check IP



```
GET https://connect.mindcloud.co/v1/universal/tophhieCloud/latest/actions/check-ip
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Tophhie Cloud `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tophhieCloud/latest/actions/check-ip?connectionId=$CONNECTION_ID&ip=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "ip": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/tophhieCloud/latest/actions/check-ip?${params}`, {
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
| `ip` | string | yes | The IP address to query. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `reverseCheck` | boolean | no | Whether to perform a reverse DNS lookup on the IP address. Default: `false`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "ipVersion": 1,
      "mapsUrl": {},
      "metadata": {},
      "result": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `ipVersion` | number | Detected IP version. |
| `mapsUrl` | object | Map links for the IP location. |
| `metadata` | object | Provider metadata for the IP lookup. |
| `result` | string | Queried IP address or location result. |

## Native endpoint

Through the native Tophhie Cloud API, this operation is `GET /IPCheck` (base URL `https://api.tophhie.cloud`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/check-ip.md) for the provider-specific parameters and requirements.

