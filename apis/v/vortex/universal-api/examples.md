# Vortex Universal API Examples

These examples use the MindCloud API key and Vortex connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Autojoin Domain By Id



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/vortex/latest/actions/get-autojoin-domain-by-id?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/vortex/latest/actions/get-autojoin-domain-by-id?${params}`, {
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
      "id": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get Autojoin Domain By Id action reference](actions/get-autojoin-domain-by-id.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/vortex/latest/actions/get-autojoin-domain-by-id).

## Accept Invitation



```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/vortex/latest/actions/accept-invitation" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/vortex/latest/actions/accept-invitation', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
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
      "invitations": [
        {
          "accountId": "string",
          "createdAt": "string",
          "deactivated": true,
          "expired": true,
          "expires": "string",
          "id": "string",
          "invitationType": "string",
          "modifiedAt": "string",
          "scope": "string",
          "scopeType": "string",
          "status": "string",
          "target": [
            {
              "avatarUrl": "https://example.com",
              "name": "Ava Chen",
              "type": "string",
              "value": "string"
            }
          ]
        }
      ]
    }
  ],
  "meta": {}
}
```

See the full [Accept Invitation action reference](actions/accept-invitation.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/vortex/latest/actions/accept-invitation).
