# EventSquare Universal API Examples

These examples use the MindCloud API key and EventSquare connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Make Account

Retrieves the connected Make account from EventSquare.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/eventSquare/latest/actions/get-make-account?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/eventSquare/latest/actions/get-make-account?${params}`, {
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
      "account": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get Make Account action reference](actions/get-make-account.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/eventSquare/latest/actions/get-make-account).

## Register Make Webhook

Registers a Make webhook in EventSquare.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/eventSquare/latest/actions/register-make-webhook" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "type": "0",
  "url": "https://example.com/webhooks/eventsquare"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/eventSquare/latest/actions/register-make-webhook', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "type": "0",
    "url": "https://example.com/webhooks/eventsquare"
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
      "status": "string"
    }
  ],
  "meta": {}
}
```

See the full [Register Make Webhook action reference](actions/register-make-webhook.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/eventSquare/latest/actions/register-make-webhook).
