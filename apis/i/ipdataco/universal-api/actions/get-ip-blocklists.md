# ipdata.co: Get IP Blocklists



```
GET https://connect.mindcloud.co/v1/universal/ipdataco/latest/actions/get-ip-blocklists
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ipdata.co `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ipdataco/latest/actions/get-ip-blocklists?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ipdataco/latest/actions/get-ip-blocklists?${params}`, {
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
| `ip` | string | no | The IP address to look up. Default: `27.126.160.0`. Example: `27.126.160.0`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "blocklists": [
        {}
      ],
      "isThreat": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `blocklists` | array<object> | Blocklist matches for the IP. |
| `isThreat` | boolean | Whether the IP is classified as a threat. |

## Native endpoint

Through the native ipdata.co API, this operation is `GET /:ip/threat` (base URL `https://api.ipdata.co`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-ip-blocklists.md) for the provider-specific parameters and requirements.

