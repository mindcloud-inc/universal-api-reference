# Abstract IBAN Validator Universal API Examples

These examples use the MindCloud API key and Abstract IBAN Validator connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Validate IBAN



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/abstractIBANValidator/latest/actions/validate-iban?connectionId=$CONNECTION_ID&iban=BE71096123456769" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "iban": "BE71096123456769"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/abstractIBANValidator/latest/actions/validate-iban?${params}`, {
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
      "iban": "string",
      "isValid": true
    }
  ],
  "meta": {}
}
```

See the full [Validate IBAN action reference](actions/validate-iban.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/abstractIBANValidator/latest/actions/validate-iban).
