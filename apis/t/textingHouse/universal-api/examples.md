# TextingHouse Universal API Examples

These examples use the MindCloud API key and TextingHouse connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Credit Balance

Retrieves the current TextingHouse credit balance.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/textingHouse/latest/actions/get-credit-balance?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/textingHouse/latest/actions/get-credit-balance?${params}`, {
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
      "creditBalance": 1,
      "rawResponse": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get Credit Balance action reference](actions/get-credit-balance.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/textingHouse/latest/actions/get-credit-balance).

## Send Commercial SMS

Creates a commercial SMS in TextingHouse.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/textingHouse/latest/actions/send-commercial-sms" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "to": "33628000000",
  "txt": "ACME: 20% off today. Reply STOP to opt out."
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/textingHouse/latest/actions/send-commercial-sms', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "to": "33628000000",
    "txt": "ACME: 20% off today. Reply STOP to opt out."
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
      "apiMessageId": "string",
      "rawResponse": "string"
    }
  ],
  "meta": {}
}
```

See the full [Send Commercial SMS action reference](actions/send-commercial-sms.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/textingHouse/latest/actions/send-commercial-sms).
