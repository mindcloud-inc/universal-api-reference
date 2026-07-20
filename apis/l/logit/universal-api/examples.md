# Logit Universal API Examples

These examples use the MindCloud API key and Logit connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Profile

Retrieves your profile from Logit.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/logit/latest/actions/get-profile?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/logit/latest/actions/get-profile?${params}`, {
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
      "apiKeys": [
        {}
      ],
      "email": "ava@example.com",
      "name": "Ava Chen",
      "userId": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get Profile action reference](actions/get-profile.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/logit/latest/actions/get-profile).

## Apply Stack Pipeline Config

Updates stack pipeline config in Logit.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/logit/latest/actions/apply-stack-pipeline-config" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "stackId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/logit/latest/actions/apply-stack-pipeline-config', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "stackId": "string"
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
      "message": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

See the full [Apply Stack Pipeline Config action reference](actions/apply-stack-pipeline-config.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/logit/latest/actions/apply-stack-pipeline-config).
