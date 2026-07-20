# Host.io: Get Domain DNS Records

Retrieves DNS records for a domain from Host.io.

```
GET https://connect.mindcloud.co/v1/universal/hostio/latest/actions/get-domain-dns-records
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Host.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hostio/latest/actions/get-domain-dns-records?connectionId=$CONNECTION_ID&domain=facebook.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "domain": "facebook.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hostio/latest/actions/get-domain-dns-records?${params}`, {
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
| `domain` | string | yes | Domain to retrieve DNS records for. Default: `facebook.com`. Example: `facebook.com`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "a": [
        "string"
      ],
      "aaaa": [
        "string"
      ],
      "domain": "string",
      "mx": [
        "string"
      ],
      "ns": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `a` | array<string> | IPv4 A records. |
| `aaaa` | array<string> | IPv6 AAAA records. |
| `domain` | string | Domain name. |
| `mx` | array<string> | MX mailserver records. |
| `ns` | array<string> | NS nameserver records. |

## Native endpoint

Through the native Host.io API, this operation is `GET /dns/:domain` (base URL `https://host.io/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-domain-dns-records.md) for the provider-specific parameters and requirements.

