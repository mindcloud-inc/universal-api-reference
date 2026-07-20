# API Template Universal API Examples

These examples use the MindCloud API key and API Template connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Query Account Information

Retrieves account information from API Template.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/aPITemplate/latest/actions/query-account-information?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/aPITemplate/latest/actions/query-account-information?${params}`, {
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

See the full [Query Account Information action reference](actions/query-account-information.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/aPITemplate/latest/actions/query-account-information).

## Create Image

Creates an image in API Template.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/aPITemplate/latest/actions/create-image" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "templateId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/aPITemplate/latest/actions/create-image', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "templateId": "string"
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

See the full [Create Image action reference](actions/create-image.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/aPITemplate/latest/actions/create-image).
