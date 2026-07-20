# ConfigCat Universal API Examples

These examples use the MindCloud API key and ConfigCat connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Authenticated User Details

Retrieves authenticated user details from ConfigCat.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/configCat/latest/actions/get-authenticated-user-details?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/configCat/latest/actions/get-authenticated-user-details?${params}`, {
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

See the full [Get Authenticated User Details action reference](actions/get-authenticated-user-details.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/configCat/latest/actions/get-authenticated-user-details).

## Create Config

Creates a new config in ConfigCat.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/configCat/latest/actions/create-config" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "productId": "string",
  "config": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/configCat/latest/actions/create-config', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "productId": "string",
    "config": {}
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

See the full [Create Config action reference](actions/create-config.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/configCat/latest/actions/create-config).
