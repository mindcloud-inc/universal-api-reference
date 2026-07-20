# Pantry Universal API Examples

These examples use the MindCloud API key and Pantry connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Pantry Details

Retrieves pantry details from Pantry.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pantry/latest/actions/get-pantry-details?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pantry/latest/actions/get-pantry-details?${params}`, {
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

See the full [Get Pantry Details action reference](actions/get-pantry-details.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/pantry/latest/actions/get-pantry-details).

## Create Or Replace Basket

Creates or replaces a basket in Pantry.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/pantry/latest/actions/create-or-replace-basket" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "basketName": "ProjectSettings",
  "contents": "[object Object]"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/pantry/latest/actions/create-or-replace-basket', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "basketName": "ProjectSettings",
    "contents": "[object Object]"
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
      "derp": "string",
      "keysLength": 1,
      "Metadata": {},
      "testPayload": true
    }
  ],
  "meta": {}
}
```

See the full [Create Or Replace Basket action reference](actions/create-or-replace-basket.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/pantry/latest/actions/create-or-replace-basket).
