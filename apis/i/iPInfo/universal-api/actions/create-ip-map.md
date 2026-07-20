# IPInfo: Create IP Map



```
POST https://connect.mindcloud.co/v1/universal/iPInfo/latest/actions/create-ip-map
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a IPInfo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/iPInfo/latest/actions/create-ip-map" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "ipAddresses": "8.8.8.8\n1.1.1.1"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/iPInfo/latest/actions/create-ip-map', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "ipAddresses": "8.8.8.8\n1.1.1.1"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `ipAddresses` | string | yes | Newline-delimited list of IP addresses to place on a map. Example: `8.8.8.8 1.1.1.1`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "reportUrl": "https://example.com",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `reportUrl` | string |  |
| `status` | string |  |

## Native endpoint

Through the native IPInfo API, this operation is `POST /tools/map` (base URL `https://api.ipinfo.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-ip-map.md) for the provider-specific parameters and requirements.

