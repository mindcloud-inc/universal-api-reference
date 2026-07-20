# API Labz: Domain Lookup

Retrieves domain information from API Labz.

```
GET https://connect.mindcloud.co/v1/universal/aPILabz/latest/actions/domain-lookup
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a API Labz `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/aPILabz/latest/actions/domain-lookup?connectionId=$CONNECTION_ID&domain=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "domain": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/aPILabz/latest/actions/domain-lookup?${params}`, {
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
      "creationdate": "string",
      "dnssec": "string",
      "domainname": "Ava Chen",
      "domainstatus": "string",
      "nameserver": "Ava Chen",
      "registrantcountry": "string",
      "registrantemail": "ava@example.com",
      "registrantorganization": "string",
      "registrar": "string",
      "registrarabusecontact": "string",
      "registrarabusecontactphone": "string",
      "registrarianaid": "string",
      "registrarregistrationexpirationdate": "string",
      "registrarurl": "https://example.com",
      "registrarwhoisserver": "string",
      "registrydomainid": "string",
      "techemail": "ava@example.com",
      "updateddate": "string",
      "urloftheicannwhoisdataproblemreportingsystem": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `creationdate` | string |  |
| `dnssec` | string |  |
| `domainname` | string |  |
| `domainstatus` | string |  |
| `nameserver` | string |  |
| `registrantcountry` | string |  |
| `registrantemail` | string |  |
| `registrantorganization` | string |  |
| `registrar` | string |  |
| `registrarabusecontact` | string |  |
| `registrarabusecontactphone` | string |  |
| `registrarianaid` | string |  |
| `registrarregistrationexpirationdate` | string |  |
| `registrarurl` | string |  |
| `registrarwhoisserver` | string |  |
| `registrydomainid` | string |  |
| `techemail` | string |  |
| `updateddate` | string |  |
| `urloftheicannwhoisdataproblemreportingsystem` | string |  |

## Native endpoint

Through the native API Labz API, this operation is `POST /module/131` (base URL `https://hub.apilabz.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/domain-lookup.md) for the provider-specific parameters and requirements.

