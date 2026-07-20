# IP2WHOIS: Lookup Domain WHOIS

Retrieves domain WHOIS details from IP2WHOIS.

```
GET https://connect.mindcloud.co/v1/universal/iP2WHOIS/latest/actions/lookup-domain-whois
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a IP2WHOIS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/iP2WHOIS/latest/actions/lookup-domain-whois?connectionId=$CONNECTION_ID&domain=example.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "domain": "example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/iP2WHOIS/latest/actions/lookup-domain-whois?${params}`, {
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
| `domain` | string | yes | Domain name to look up. Example: `example.com`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "admin": {
        "city": "string",
        "country": "string",
        "email": "ava@example.com",
        "fax": "string",
        "name": "Ava Chen",
        "organization": "string",
        "phone": "string",
        "region": "string",
        "streetAddress": "string",
        "zipCode": "string"
      },
      "billing": {
        "city": "string",
        "country": "string",
        "email": "ava@example.com",
        "fax": "string",
        "name": "Ava Chen",
        "organization": "string",
        "phone": "string",
        "region": "string",
        "streetAddress": "string",
        "zipCode": "string"
      },
      "createDate": "2026-05-07T12:00:00.000Z",
      "domain": "string",
      "domainAge": 1,
      "domainId": "string",
      "expireDate": "2026-05-07T12:00:00.000Z",
      "nameservers": [
        "Ava Chen"
      ],
      "registrant": {
        "city": "string",
        "country": "string",
        "email": "ava@example.com",
        "fax": "string",
        "name": "Ava Chen",
        "organization": "string",
        "phone": "string",
        "region": "string",
        "streetAddress": "string",
        "zipCode": "string"
      },
      "registrar": {
        "ianaId": "string",
        "name": "Ava Chen",
        "url": "https://example.com"
      },
      "status": "string",
      "tech": {
        "city": "string",
        "country": "string",
        "email": "ava@example.com",
        "fax": "string",
        "name": "Ava Chen",
        "organization": "string",
        "phone": "string",
        "region": "string",
        "streetAddress": "string",
        "zipCode": "string"
      },
      "updateDate": "2026-05-07T12:00:00.000Z",
      "whoisServer": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `admin` | object |  |
| `admin.city` | string |  |
| `admin.country` | string |  |
| `admin.email` | string |  |
| `admin.fax` | string |  |
| `admin.name` | string |  |
| `admin.organization` | string |  |
| `admin.phone` | string |  |
| `admin.region` | string |  |
| `admin.streetAddress` | string |  |
| `admin.zipCode` | string |  |
| `billing` | object |  |
| `billing.city` | string |  |
| `billing.country` | string |  |
| `billing.email` | string |  |
| `billing.fax` | string |  |
| `billing.name` | string |  |
| `billing.organization` | string |  |
| `billing.phone` | string |  |
| `billing.region` | string |  |
| `billing.streetAddress` | string |  |
| `billing.zipCode` | string |  |
| `createDate` | date |  |
| `domain` | string |  |
| `domainAge` | number |  |
| `domainId` | string |  |
| `expireDate` | date |  |
| `nameservers` | array<string> |  |
| `registrant` | object |  |
| `registrant.city` | string |  |
| `registrant.country` | string |  |
| `registrant.email` | string |  |
| `registrant.fax` | string |  |
| `registrant.name` | string |  |
| `registrant.organization` | string |  |
| `registrant.phone` | string |  |
| `registrant.region` | string |  |
| `registrant.streetAddress` | string |  |
| `registrant.zipCode` | string |  |
| `registrar` | object |  |
| `registrar.ianaId` | string |  |
| `registrar.name` | string |  |
| `registrar.url` | string |  |
| `status` | string |  |
| `tech` | object |  |
| `tech.city` | string |  |
| `tech.country` | string |  |
| `tech.email` | string |  |
| `tech.fax` | string |  |
| `tech.name` | string |  |
| `tech.organization` | string |  |
| `tech.phone` | string |  |
| `tech.region` | string |  |
| `tech.streetAddress` | string |  |
| `tech.zipCode` | string |  |
| `updateDate` | date |  |
| `whoisServer` | string |  |

## Native endpoint

Through the native IP2WHOIS API, this operation is `GET /v2` (base URL `https://api.ip2whois.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/lookup-domain-whois.md) for the provider-specific parameters and requirements.

