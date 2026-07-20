# IdentityCheck Universal API Examples

These examples use the MindCloud API key and IdentityCheck connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Verifications



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/identityCheck/latest/actions/list-verifications?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/identityCheck/latest/actions/list-verifications?${params}`, {
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
      "created_at": "2026-05-07T12:00:00.000Z",
      "email": "ava@example.com",
      "first_name": "Ava",
      "id": "string",
      "last_name": "Chen",
      "result": "string",
      "type": "string",
      "updated_at": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

See the full [List Verifications action reference](actions/list-verifications.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/identityCheck/latest/actions/list-verifications).

## Create Direct Verification



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/identityCheck/latest/actions/create-direct-verification" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "email": "ava@example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/identityCheck/latest/actions/create-direct-verification', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "email": "ava@example.com"
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
      "accountName": "Ava Chen",
      "email": "ava@example.com",
      "firstName": "Ava",
      "id": "string",
      "lastName": "Chen",
      "triggeredBy": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

See the full [Create Direct Verification action reference](actions/create-direct-verification.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/identityCheck/latest/actions/create-direct-verification).
