# Feathery Universal API Examples

These examples use the MindCloud API key and Feathery connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Retrieve Account Information



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/feathery/latest/actions/retrieve-account-information?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/feathery/latest/actions/retrieve-account-information?${params}`, {
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
      "accounts": [
        {}
      ],
      "team": "string"
    }
  ],
  "meta": {}
}
```

See the full [Retrieve Account Information action reference](actions/retrieve-account-information.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/feathery/latest/actions/retrieve-account-information).

## Copy a Form



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/feathery/latest/actions/copy-a-form" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "form_name": "Ava Chen",
  "copy_form_id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/feathery/latest/actions/copy-a-form', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "form_name": "Ava Chen",
    "copy_form_id": "string"
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
      "active": true,
      "created_at": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "internal_id": "string",
      "name": "Ava Chen",
      "tags": [
        "string"
      ],
      "updated_at": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

See the full [Copy a Form action reference](actions/copy-a-form.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/feathery/latest/actions/copy-a-form).
