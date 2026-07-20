# People Data Labs: Enrich IP



```
GET https://connect.mindcloud.co/v1/universal/peopleDataLabs/latest/actions/enrich-ip
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a People Data Labs `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/peopleDataLabs/latest/actions/enrich-ip?connectionId=$CONNECTION_ID&ip=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "ip": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/peopleDataLabs/latest/actions/enrich-ip?${params}`, {
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
| `ip` | string | yes | IPv4 or IPv6 address to enrich. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `return_if_unmatched` | boolean | no | Return IP-specific metadata or location data even when no company match is found. |
| `return_ip_location` | boolean | no | Return IP-specific location info regardless of a company match. |
| `return_ip_metadata` | boolean | no | Return IP-specific metadata regardless of a company match. |
| `return_person` | boolean | no | Return person fields associated with the IP when available. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "datasetVersion": "string",
      "ip": {
        "address": "string",
        "location": {
          "continent": "string",
          "country": "string",
          "geo": "string",
          "locality": "string",
          "metro": "string",
          "name": "Ava Chen",
          "postalCode": "string",
          "region": "string",
          "timezone": "string"
        },
        "metadata": {
          "hosting": true,
          "mobile": true,
          "proxy": true,
          "relay": true,
          "tor": true,
          "version": 1,
          "vpn": true
        }
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `datasetVersion` | string |  |
| `ip.address` | string |  |
| `ip.location.continent` | string |  |
| `ip.location.country` | string |  |
| `ip.location.geo` | string |  |
| `ip.location.locality` | string |  |
| `ip.location.metro` | string |  |
| `ip.location.name` | string |  |
| `ip.location.postalCode` | string |  |
| `ip.location.region` | string |  |
| `ip.location.timezone` | string |  |
| `ip.metadata.hosting` | boolean |  |
| `ip.metadata.mobile` | boolean |  |
| `ip.metadata.proxy` | boolean |  |
| `ip.metadata.relay` | boolean |  |
| `ip.metadata.tor` | boolean |  |
| `ip.metadata.version` | number |  |
| `ip.metadata.vpn` | boolean |  |

## Native endpoint

Through the native People Data Labs API, this operation is `GET /ip/enrich` (base URL `https://api.peopledatalabs.com/v5`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/enrich-ip.md) for the provider-specific parameters and requirements.

