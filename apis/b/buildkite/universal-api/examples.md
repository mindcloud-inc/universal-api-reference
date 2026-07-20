# Buildkite Universal API Examples

These examples use the MindCloud API key and Buildkite connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Current Access Token

Retrieves the current access token from Buildkite.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/buildkite/latest/actions/get-current-access-token?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/buildkite/latest/actions/get-current-access-token?${params}`, {
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
      "createdAt": "string",
      "description": "string",
      "expiresAt": "string",
      "scopes": [
        "string"
      ],
      "user": {
        "email": "ava@example.com",
        "name": "Ava Chen"
      },
      "uuid": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get Current Access Token action reference](actions/get-current-access-token.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/buildkite/latest/actions/get-current-access-token).

## Cancel Build

Cancels an existing build in Buildkite.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/buildkite/latest/actions/cancel-build" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "build": "string",
  "organization": "string",
  "pipeline": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/buildkite/latest/actions/cancel-build', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "build": "string",
    "organization": "string",
    "pipeline": "string"
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
      "id": "string",
      "number": 1,
      "state": "string",
      "webUrl": "https://example.com"
    }
  ],
  "meta": {}
}
```

See the full [Cancel Build action reference](actions/cancel-build.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/buildkite/latest/actions/cancel-build).
