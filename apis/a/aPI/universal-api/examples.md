# 44API Universal API Examples

These examples use the MindCloud API key and 44API connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Validate VAT Number

Validates a VAT number with 44API and returns company details.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/aPI/latest/actions/validate-vat-number?connectionId=$CONNECTION_ID&vatNumber=string&countryCode=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "vatNumber": "string",
  "countryCode": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/aPI/latest/actions/validate-vat-number?${params}`, {
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
      "cachedAt": "2026-05-07T12:00:00.000Z",
      "company": {
        "address": "string",
        "name": "Ava Chen"
      },
      "countryCode": "string",
      "valid": true,
      "vatNumber": "string",
      "verificationDate": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

See the full [Validate VAT Number action reference](actions/validate-vat-number.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/aPI/latest/actions/validate-vat-number).

## Manage IP Whitelist

Manages the IP whitelist in 44API by adding, removing, or listing IPs.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/aPI/latest/actions/manage-ip-whitelist" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "action": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/aPI/latest/actions/manage-ip-whitelist', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "action": "string"
  })
});

const { success, data } = await response.json();
```

Example response:

```json
{
  "success": true,
  "data": [],
  "meta": {}
}
```

See the full [Manage IP Whitelist action reference](actions/manage-ip-whitelist.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/aPI/latest/actions/manage-ip-whitelist).
