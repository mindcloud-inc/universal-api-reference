# Paradym Universal API Examples

These examples use the MindCloud API key and Paradym connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Projects

Retrieves a list of projects from Paradym.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/paradym/latest/actions/list-projects?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/paradym/latest/actions/list-projects?${params}`, {
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
      "data": [
        {
          "createdAt": "string",
          "id": "string",
          "name": "Ava Chen",
          "ownerId": "string",
          "updatedAt": "string",
          "verificationDataAccess": "string"
        }
      ],
      "meta": {
        "page": {
          "maxSize": "string",
          "size": "string"
        },
        "sort": [
          {
            "id": "string"
          }
        ]
      }
    }
  ],
  "meta": {}
}
```

See the full [List Projects action reference](actions/list-projects.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/paradym/latest/actions/list-projects).

## Batch Revoke Credentials

Revokes issued credentials in bulk in Paradym.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/paradym/latest/actions/batch-revoke-credentials" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "issuedCredentialIds[0]": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/paradym/latest/actions/batch-revoke-credentials', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "issuedCredentialIds[0]": "string"
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

See the full [Batch Revoke Credentials action reference](actions/batch-revoke-credentials.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/paradym/latest/actions/batch-revoke-credentials).
