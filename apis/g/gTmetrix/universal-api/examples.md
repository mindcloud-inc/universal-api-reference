# GTmetrix Universal API Examples

These examples use the MindCloud API key and GTmetrix connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Account Status

Retrieves your current GTmetrix account status.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/gTmetrix/latest/actions/get-account-status?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/gTmetrix/latest/actions/get-account-status?${params}`, {
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
      "data": {
        "attributes": {
          "account_pro_analysis_options_access": true,
          "account_pro_locations_access": true,
          "account_type": "string",
          "account_whitelabel_pdf_access": true,
          "api_credits": 1,
          "api_refill": 1,
          "api_refill_amount": 1
        },
        "id": "string",
        "type": "string"
      }
    }
  ],
  "meta": {}
}
```

See the full [Get Account Status action reference](actions/get-account-status.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/gTmetrix/latest/actions/get-account-status).
