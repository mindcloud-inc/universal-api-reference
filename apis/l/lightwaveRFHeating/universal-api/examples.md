# LightwaveRF Heating Universal API Examples

These examples use the MindCloud API key and LightwaveRF Heating connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get User Info

Retrieves the current user's account details from LightwaveRF Heating.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/lightwaveRFHeating/latest/actions/get-user-info?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/lightwaveRFHeating/latest/actions/get-user-info?${params}`, {
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
      "email": "ava@example.com",
      "userId": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get User Info action reference](actions/get-user-info.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/lightwaveRFHeating/latest/actions/get-user-info).

## Batch Write Heating Features

Updates multiple heating features in LightwaveRF Heating.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/lightwaveRFHeating/latest/actions/batch-write-heating-features" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "features[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/lightwaveRFHeating/latest/actions/batch-write-heating-features', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "features[]": [{}]
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
      "features": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

See the full [Batch Write Heating Features action reference](actions/batch-write-heating-features.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/lightwaveRFHeating/latest/actions/batch-write-heating-features).
