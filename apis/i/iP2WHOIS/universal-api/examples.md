# IP2WHOIS Universal API Examples

These examples use the MindCloud API key and IP2WHOIS connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Lookup Domain WHOIS

Retrieves domain WHOIS details from IP2WHOIS.

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

Example response:

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

See the full [Lookup Domain WHOIS action reference](actions/lookup-domain-whois.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/iP2WHOIS/latest/actions/lookup-domain-whois).
