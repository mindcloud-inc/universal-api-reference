# IPInfo: Get Lite IP Field



```
GET https://connect.mindcloud.co/v1/universal/iPInfo/latest/actions/get-lite-ip-field
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a IPInfo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/iPInfo/latest/actions/get-lite-ip-field?connectionId=$CONNECTION_ID&ip=8.8.8.8&field=country_code" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "ip": "8.8.8.8",
  "field": "country_code"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/iPInfo/latest/actions/get-lite-ip-field?${params}`, {
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
| `ip` | string | yes | IPv4 or IPv6 address to look up. Example: `8.8.8.8`. |
| `field` | string | yes | Lite field path to return, for example country_code or asn. Example: `country_code`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "response": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `response` | string |  |

## Native endpoint

Through the native IPInfo API, this operation is `GET /lite/:ip/:field` (base URL `https://api.ipinfo.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-lite-ip-field.md) for the provider-specific parameters and requirements.

