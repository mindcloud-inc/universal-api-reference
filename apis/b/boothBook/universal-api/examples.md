# BoothBook Universal API Examples

These examples use the MindCloud API key and BoothBook connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Account

Retrieves account details from BoothBook.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/boothBook/latest/actions/get-account?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/boothBook/latest/actions/get-account?${params}`, {
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
      "affiliate": "string",
      "business_address": "string",
      "business_admin": "string",
      "business_country": "string",
      "business_name": "Ava Chen",
      "business_postcode": "string",
      "business_timezone": "string",
      "business_website": "string",
      "currency_code": "string",
      "currency_sign": "string",
      "is_paid": 1,
      "plan": "string",
      "result": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get Account action reference](actions/get-account.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/boothBook/latest/actions/get-account).
