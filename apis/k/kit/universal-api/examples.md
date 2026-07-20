# Kit Universal API Examples

These examples use the MindCloud API key and Kit connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Broadcast

Retrieves a broadcast record from Kit.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/kit/latest/actions/get-broadcast?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/kit/latest/actions/get-broadcast?${params}`, {
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
      "broadcast": {}
    }
  ],
  "meta": {}
}
```

See the full [Get Broadcast action reference](actions/get-broadcast.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/kit/latest/actions/get-broadcast).

## Add Subscriber to Form

Adds an existing subscriber to a Kit form.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/kit/latest/actions/add-subscriber-to-form" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "formId": "12345",
  "emailAddress": "subscriber@example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/kit/latest/actions/add-subscriber-to-form', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "formId": "12345",
    "emailAddress": "subscriber@example.com"
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
      "subscriber": {}
    }
  ],
  "meta": {}
}
```

See the full [Add Subscriber to Form action reference](actions/add-subscriber-to-form.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/kit/latest/actions/add-subscriber-to-form).
