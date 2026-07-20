# Companies House Universal API Examples

These examples use the MindCloud API key and Companies House connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Company Profile

Retrieves a company profile from Companies House.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/companiesHouse/latest/actions/get-company-profile?connectionId=$CONNECTION_ID&companyNumber=00000006" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "companyNumber": "00000006"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/companiesHouse/latest/actions/get-company-profile?${params}`, {
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
      "accounts": {},
      "can_file": true,
      "company_name": "Ava Chen",
      "company_number": "string",
      "company_status": "string",
      "confirmation_statement": {},
      "date_of_creation": "string",
      "etag": "string",
      "has_been_liquidated": true,
      "has_charges": true,
      "has_insolvency_history": true,
      "has_super_secure_pscs": true,
      "jurisdiction": "string",
      "links": {},
      "registered_office_address": {},
      "sic_codes": [
        "string"
      ],
      "type": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get Company Profile action reference](actions/get-company-profile.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/companiesHouse/latest/actions/get-company-profile).
