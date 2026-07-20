# MyEmailVerifier Universal API Examples

These examples use the MindCloud API key and MyEmailVerifier connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Credits

Retrieves remaining verification credits from MyEmailVerifier.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/myEmailVerifier/latest/actions/get-credits?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/myEmailVerifier/latest/actions/get-credits?${params}`, {
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
      "credits": 1,
      "status": true
    }
  ],
  "meta": {}
}
```

See the full [Get Credits action reference](actions/get-credits.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/myEmailVerifier/latest/actions/get-credits).

## Upload Verification File

Creates a bulk verification upload in MyEmailVerifier.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/myEmailVerifier/latest/actions/upload-verification-file" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "filename": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/myEmailVerifier/latest/actions/upload-verification-file', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "filename": "Ava Chen"
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
      "data": {},
      "file_id": 1,
      "file_name": "Ava Chen",
      "message": "string",
      "status": true
    }
  ],
  "meta": {}
}
```

See the full [Upload Verification File action reference](actions/upload-verification-file.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/myEmailVerifier/latest/actions/upload-verification-file).
