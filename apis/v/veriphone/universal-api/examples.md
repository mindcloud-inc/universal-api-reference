# Veriphone Universal API Examples

These examples use the MindCloud API key and Veriphone connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Example Phone Number



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/veriphone/latest/actions/get-example-phone-number?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/veriphone/latest/actions/get-example-phone-number?${params}`, {
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
      "country_code": "string",
      "country_prefix": 1,
      "e164": "string",
      "international_number": "string",
      "local_number": "string",
      "phone_type": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get Example Phone Number action reference](actions/get-example-phone-number.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/veriphone/latest/actions/get-example-phone-number).
