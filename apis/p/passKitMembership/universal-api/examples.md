# PassKit Membership Universal API Examples

These examples use the MindCloud API key and PassKit Membership connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Programs

Retrieves membership programs from PassKit Membership.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/passKitMembership/latest/actions/list-programs?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/passKitMembership/latest/actions/list-programs?${params}`, {
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
      "created": "string",
      "id": "string",
      "localizedName": "Ava Chen",
      "name": "Ava Chen",
      "passTypeIdentifier": "string",
      "profileImageSettings": "string",
      "status": [
        "string"
      ],
      "updated": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Programs action reference](actions/list-programs.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/passKitMembership/latest/actions/list-programs).

## Create Member

Creates a member in PassKit Membership.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/passKitMembership/latest/actions/create-member" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "displayName": "Ava Chen",
  "externalId": "string",
  "programId": "string",
  "tierId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/passKitMembership/latest/actions/create-member', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "displayName": "Ava Chen",
    "externalId": "string",
    "programId": "string",
    "tierId": "string"
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
      "id": "string"
    }
  ],
  "meta": {}
}
```

See the full [Create Member action reference](actions/create-member.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/passKitMembership/latest/actions/create-member).
