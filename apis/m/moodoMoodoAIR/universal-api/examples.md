# Moodo & Moodo AIR Universal API Examples

These examples use the MindCloud API key and Moodo & Moodo AIR connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Boxes

Retrieves Moodo boxes available to the current user.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/moodoMoodoAIR/latest/actions/list-boxes?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/moodoMoodoAIR/latest/actions/list-boxes?${params}`, {
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
      "boxes": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

See the full [List Boxes action reference](actions/list-boxes.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/moodoMoodoAIR/latest/actions/list-boxes).

## Accept Terms And Conditions

Accepts the Terms and Conditions in Moodo.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/moodoMoodoAIR/latest/actions/accept-terms-and-conditions" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/moodoMoodoAIR/latest/actions/accept-terms-and-conditions', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
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
      "accepted": true
    }
  ],
  "meta": {}
}
```

See the full [Accept Terms And Conditions action reference](actions/accept-terms-and-conditions.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/moodoMoodoAIR/latest/actions/accept-terms-and-conditions).
