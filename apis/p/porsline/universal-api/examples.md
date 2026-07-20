# Porsline Universal API Examples

These examples use the MindCloud API key and Porsline connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Folders



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/porsline/latest/actions/list-folders?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/porsline/latest/actions/list-folders?${params}`, {
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
  "data": [],
  "meta": {}
}
```

See the full [List Folders action reference](actions/list-folders.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/porsline/latest/actions/list-folders).

## Create Authentication Codes



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/porsline/latest/actions/create-authentication-codes" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "survey_id": 1,
  "codes": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/porsline/latest/actions/create-authentication-codes', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "survey_id": 1,
    "codes": "string"
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
      "value": "string"
    }
  ],
  "meta": {}
}
```

See the full [Create Authentication Codes action reference](actions/create-authentication-codes.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/porsline/latest/actions/create-authentication-codes).
