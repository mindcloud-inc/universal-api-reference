# Deepgram Universal API Examples

These examples use the MindCloud API key and Deepgram connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Token Details

Retrieves API token details from Deepgram.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/deepgram/latest/actions/get-token-details?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/deepgram/latest/actions/get-token-details?${params}`, {
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
      "accessor": "string",
      "accessorGeneration": 1,
      "created": "string",
      "email": "ava@example.com",
      "firstName": "Ava",
      "lastName": "Chen",
      "scopes": [
        "string"
      ],
      "subject": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get Token Details action reference](actions/get-token-details.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/deepgram/latest/actions/get-token-details).

## Create Project Key

Creates a new project API key in Deepgram.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/deepgram/latest/actions/create-project-key" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "projectId": "string",
  "scopes": "string",
  "expirationDate": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/deepgram/latest/actions/create-project-key', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "projectId": "string",
    "scopes": "string",
    "expirationDate": "string"
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
      "apiKeyId": "string",
      "comment": "string",
      "created": "string",
      "expirationDate": "string",
      "key": "string",
      "scopes": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

See the full [Create Project Key action reference](actions/create-project-key.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/deepgram/latest/actions/create-project-key).
