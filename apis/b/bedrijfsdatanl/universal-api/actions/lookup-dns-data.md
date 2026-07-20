# Bedrijfsdata.nl: Lookup DNS Data



```
GET https://connect.mindcloud.co/v1/universal/bedrijfsdatanl/latest/actions/lookup-dns-data
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bedrijfsdata.nl `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bedrijfsdatanl/latest/actions/lookup-dns-data?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bedrijfsdatanl/latest/actions/lookup-dns-data?${params}`, {
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
| `domain` | string | no | Domain to inspect for DNS records. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "creditsUsed": 1,
      "creditsUsedMonth": 1,
      "dns": {
        "dnsA": [
          "string"
        ],
        "dnsMx": [
          "string"
        ],
        "dnsNs": [
          "string"
        ],
        "dnsserver": "string",
        "dnsSoa": [
          "string"
        ],
        "dnsTxt": [
          "string"
        ],
        "dnsWwwA": [
          "string"
        ],
        "dnsWwwCname": [
          "Ava Chen"
        ],
        "domain": "string",
        "host": "string",
        "hostType": "string",
        "ip": "string",
        "ipint": 1,
        "mailserver": "string",
        "spf": "string"
      },
      "monthlyCredits": 1,
      "product": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `creditsUsed` | number |  |
| `creditsUsedMonth` | number |  |
| `dns.dnsA[]` | string |  |
| `dns.dnsMx[]` | string |  |
| `dns.dnsNs[]` | string |  |
| `dns.dnsserver` | string |  |
| `dns.dnsSoa[]` | string |  |
| `dns.dnsTxt[]` | string |  |
| `dns.dnsWwwA[]` | string |  |
| `dns.dnsWwwCname[]` | string |  |
| `dns.domain` | string |  |
| `dns.host` | string |  |
| `dns.hostType` | string |  |
| `dns.ip` | string |  |
| `dns.ipint` | number |  |
| `dns.mailserver` | string |  |
| `dns.spf` | string |  |
| `monthlyCredits` | number |  |
| `product` | string |  |
| `status` | string |  |

## Native endpoint

Through the native Bedrijfsdata.nl API, this operation is `GET /dns` (base URL `https://fapi.bedrijfsdata.nl/v1.2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/lookup-dns-data.md) for the provider-specific parameters and requirements.

