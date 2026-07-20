# IP2WHOIS: List Hosted Domains by IP

Finds hosted domains in IP2WHOIS by IP address.

```
GET https://connect.mindcloud.co/v1/universal/iP2WHOIS/latest/actions/list-hosted-domains-by-ip
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a IP2WHOIS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/iP2WHOIS/latest/actions/list-hosted-domains-by-ip?connectionId=$CONNECTION_ID&ip=8.8.8.8" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "ip": "8.8.8.8"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/iP2WHOIS/latest/actions/list-hosted-domains-by-ip?${params}`, {
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

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `page` | number | no | Page number for hosted domain results. Example: `1`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "domains": [
        "string"
      ],
      "ip": "string",
      "page": 1,
      "perPage": 1,
      "totalDomains": 1,
      "totalPages": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `domains` | array<string> |  |
| `ip` | string |  |
| `page` | number |  |
| `perPage` | number |  |
| `totalDomains` | number |  |
| `totalPages` | number |  |

## Native endpoint

Through the native IP2WHOIS API, this operation is `GET https://domains.ip2whois.com/domains` (base URL `https://api.ip2whois.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-hosted-domains-by-ip.md) for the provider-specific parameters and requirements.

