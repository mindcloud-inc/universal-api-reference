# Loqate: Detect Country From IP Address

Detects a country from an IP address with Loqate.

```
GET https://connect.mindcloud.co/v1/universal/loqate/latest/actions/detect-country-from-ip-address
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Loqate `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/loqate/latest/actions/detect-country-from-ip-address?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/loqate/latest/actions/detect-country-from-ip-address?${params}`, {
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
| `ipAddress` | string | no | The IP address to check. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "country": "string",
      "ipAddress": "string",
      "iso2": "string",
      "iso3": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `country` | string |  |
| `ipAddress` | string |  |
| `iso2` | string |  |
| `iso3` | string |  |

## Native endpoint

Through the native Loqate API, this operation is `GET /Extras/Web/Ip2Country/v1.10/json6.ws` (base URL `https://api.addressy.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/detect-country-from-ip-address.md) for the provider-specific parameters and requirements.

