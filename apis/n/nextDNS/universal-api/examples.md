# NextDNS Universal API Examples

These examples use the MindCloud API key and NextDNS connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Profile

Retrieves a configuration profile from NextDNS.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/nextDNS/latest/actions/get-profile?connectionId=$CONNECTION_ID&profileId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "profileId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/nextDNS/latest/actions/get-profile?${params}`, {
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
      "allowlist": [
        {}
      ],
      "denylist": [
        {}
      ],
      "fingerprint": "string",
      "id": "string",
      "name": "Ava Chen",
      "parentalControl": {},
      "privacy": {},
      "rewrites": [
        {}
      ],
      "security": {},
      "settings": {},
      "setup": {}
    }
  ],
  "meta": {}
}
```

See the full [Get Profile action reference](actions/get-profile.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/nextDNS/latest/actions/get-profile).

## Add Allowlist Domain

Creates an allowlist domain entry in a NextDNS profile.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/nextDNS/latest/actions/add-allowlist-domain" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "profileId": "string",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/nextDNS/latest/actions/add-allowlist-domain', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "profileId": "string",
    "id": "string"
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

See the full [Add Allowlist Domain action reference](actions/add-allowlist-domain.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/nextDNS/latest/actions/add-allowlist-domain).
