# Lettr: Get Domain



```
GET https://connect.mindcloud.co/v1/universal/lettr/latest/actions/get-domain
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Lettr `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/lettr/latest/actions/get-domain?connectionId=$CONNECTION_ID&domain=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "domain": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/lettr/latest/actions/get-domain?${params}`, {
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
| `domain` | string | yes | Sending domain name. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "can_send": true,
        "cname_status": "Ava Chen",
        "created_at": "2026-05-07T12:00:00.000Z",
        "dkim_status": "string",
        "dmarc_status": "string",
        "dns": {
          "dkim": {
            "headers": "string",
            "public": "string",
            "selector": "string"
          }
        },
        "dns_provider": "string",
        "domain": "string",
        "is_primary_domain": true,
        "spf_status": "string",
        "status": "string",
        "status_label": "string",
        "tracking_domain": "string",
        "updated_at": "2026-05-07T12:00:00.000Z"
      },
      "message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object | Domain payload. |
| `data.can_send` | boolean | Whether the domain can send mail. |
| `data.cname_status` | string | Tracking CNAME status when present. |
| `data.created_at` | date | Creation timestamp. |
| `data.dkim_status` | string | DKIM verification status when present. |
| `data.dmarc_status` | string | DMARC verification status when present. |
| `data.dns` | object | DNS setup details. |
| `data.dns_provider` | string | Detected DNS provider when present. |
| `data.dns.dkim` | object | DKIM DNS details. |
| `data.dns.dkim.headers` | string | DKIM signed headers. |
| `data.dns.dkim.public` | string | DKIM public key. |
| `data.dns.dkim.selector` | string | DKIM selector. |
| `data.domain` | string | Sending domain name. |
| `data.is_primary_domain` | boolean | Whether this is the primary domain. |
| `data.spf_status` | string | SPF verification status when present. |
| `data.status` | string | Domain status code. |
| `data.status_label` | string | Human-readable domain status. |
| `data.tracking_domain` | string | Associated tracking domain when present. |
| `data.updated_at` | date | Last update timestamp. |
| `message` | string | Domain retrieval status message. |

## Native endpoint

Through the native Lettr API, this operation is `GET /domains/:domain` (base URL `https://app.lettr.com/api/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-domain.md) for the provider-specific parameters and requirements.

