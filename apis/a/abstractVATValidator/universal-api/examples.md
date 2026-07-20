# Abstract VAT Validator Universal API Examples

These examples use the MindCloud API key and Abstract VAT Validator connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Validate VAT Number

Validates a VAT number and returns company details from Abstract VAT Validator.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/abstractVATValidator/latest/actions/validate-vat-number?connectionId=$CONNECTION_ID&vat_number=SE556656688001" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "vat_number": "SE556656688001"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/abstractVATValidator/latest/actions/validate-vat-number?${params}`, {
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
      "company": {
        "address": "string",
        "name": "Ava Chen"
      },
      "country": {
        "code": "string",
        "name": "Ava Chen"
      },
      "valid": true,
      "vat_number": "string"
    }
  ],
  "meta": {}
}
```

See the full [Validate VAT Number action reference](actions/validate-vat-number.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/abstractVATValidator/latest/actions/validate-vat-number).
