# D7 Networks Universal API Examples

These examples use the MindCloud API key and D7 Networks connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get SMS Pricing

Retrieves SMS pricing details from D7 Networks.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/d7Networks/latest/actions/get-sms-pricing?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/d7Networks/latest/actions/get-sms-pricing?${params}`, {
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
      "countryIso": "string",
      "price": 1
    }
  ],
  "meta": {}
}
```

See the full [Get SMS Pricing action reference](actions/get-sms-pricing.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/d7Networks/latest/actions/get-sms-pricing).

## Resend OTP

Resends a one-time password with D7 Networks.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/d7Networks/latest/actions/resend-otp" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "otp_id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/d7Networks/latest/actions/resend-otp', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "otp_id": "string"
  })
});

const { success, data } = await response.json();
```

Example response:

```json
{
  "success": true,
  "data": [
    {
      "expiry": 1,
      "otp_id": "string",
      "resend_count": 1,
      "status": "string"
    }
  ],
  "meta": {}
}
```

See the full [Resend OTP action reference](actions/resend-otp.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/d7Networks/latest/actions/resend-otp).
