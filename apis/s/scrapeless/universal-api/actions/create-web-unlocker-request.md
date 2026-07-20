# Scrapeless: Create Web Unlocker Request

Creates a web unlocker request in Scrapeless.

```
POST https://connect.mindcloud.co/v1/universal/scrapeless/latest/actions/create-web-unlocker-request
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Scrapeless `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/scrapeless/latest/actions/create-web-unlocker-request" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "input": {},
  "input.url": "https://example.com",
  "input.method": "string",
  "proxy": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/scrapeless/latest/actions/create-web-unlocker-request', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "input": {},
    "input.url": "https://example.com",
    "input.method": "string",
    "proxy": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `input` | object | yes |  |
| `input.url` | string | yes | request url |
| `input.redirect` | boolean | no | whether redirect request |
| `input.method` | string | yes | request method |
| `input.header` | object | no | request headers |
| `proxy` | object | yes | proxy info |
| `proxy.country` | string | no | proxy country, see more in [Scrapeless proxy documentation](https://docs.scrapeless.com/en/proxies/features/proxy/) |
| `proxy.url` | string | no | proxy url |

## Response

```json
{
  "success": true,
  "data": [
    {
      "code": 1,
      "data": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `code` | number |  |
| `data` | string |  |

## Native endpoint

Through the native Scrapeless API, this operation is `POST /api/v2/unlocker/request` (base URL `https://api.scrapeless.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-web-unlocker-request.md) for the provider-specific parameters and requirements.

