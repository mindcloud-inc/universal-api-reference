# Sertifier Universal API Examples

These examples use the MindCloud API key and Sertifier connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Test Authentication

Tests the current authentication setup for Sertifier.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sertifier/latest/actions/test-authentication?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sertifier/latest/actions/test-authentication?${params}`, {
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
      "hasError": true,
      "message": "string"
    }
  ],
  "meta": {}
}
```

See the full [Test Authentication action reference](actions/test-authentication.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/sertifier/latest/actions/test-authentication).

## Add Attribute

Creates a new attribute in Sertifier.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/sertifier/latest/actions/add-attribute" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "title": "string",
  "type": "1"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/sertifier/latest/actions/add-attribute', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "title": "string",
    "type": "1"
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
      "response": "string"
    }
  ],
  "meta": {}
}
```

See the full [Add Attribute action reference](actions/add-attribute.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/sertifier/latest/actions/add-attribute).
