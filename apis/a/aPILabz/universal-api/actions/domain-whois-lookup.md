# API Labz: Domain WHOIS Lookup

Retrieves WHOIS details for a domain in API Labz.

```
GET https://connect.mindcloud.co/v1/universal/aPILabz/latest/actions/domain-whois-lookup
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a API Labz `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/aPILabz/latest/actions/domain-whois-lookup?connectionId=$CONNECTION_ID&domain=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "domain": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/aPILabz/latest/actions/domain-whois-lookup?${params}`, {
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
| `domain` | string | yes | Domain name to lookup |

## Response

```json
{
  "success": true,
  "data": [
    {
      "creationDate": "string",
      "dnssec": "string",
      "domainName": "Ava Chen",
      "domainStatuses": [
        "string"
      ],
      "expirationDate": "string",
      "nameServers": [
        "Ava Chen"
      ],
      "registrantCountry": "string",
      "registrantOrganization": "string",
      "registrar": "string",
      "registrarAbuseContactPhone": "string",
      "registrarIanaId": "string",
      "registrarUrl": "https://example.com",
      "registrarWhoisServer": "string",
      "registryDomainId": "string",
      "updatedDate": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `creationDate` | string |  |
| `dnssec` | string |  |
| `domainName` | string |  |
| `domainStatuses` | array<string> |  |
| `expirationDate` | string |  |
| `nameServers` | array<string> |  |
| `registrantCountry` | string |  |
| `registrantOrganization` | string |  |
| `registrar` | string |  |
| `registrarAbuseContactPhone` | string |  |
| `registrarIanaId` | string |  |
| `registrarUrl` | string |  |
| `registrarWhoisServer` | string |  |
| `registryDomainId` | string |  |
| `updatedDate` | string |  |

## Native endpoint

Through the native API Labz API, this operation is `POST /module/614` (base URL `https://hub.apilabz.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/domain-whois-lookup.md) for the provider-specific parameters and requirements.

