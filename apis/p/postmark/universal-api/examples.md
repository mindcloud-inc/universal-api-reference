# Postmark Universal API Examples

These examples use the MindCloud API key and Postmark connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Templates

Retrieves templates from Postmark.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/postmark/latest/actions/list-templates?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/postmark/latest/actions/list-templates?${params}`, {
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
      "Templates": [
        [
          {}
        ]
      ],
      "TotalCount": 1
    }
  ],
  "meta": {}
}
```

See the full [List Templates action reference](actions/list-templates.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/postmark/latest/actions/list-templates).

## Create Domain

Creates a domain in Postmark.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/postmark/latest/actions/create-domain" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/postmark/latest/actions/create-domain', {
  method: 'POST',
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
      "DKIMPendingHost": "string",
      "DKIMVerified": true,
      "ID": 1,
      "Name": "Ava Chen",
      "ReturnPathDomain": "string",
      "ReturnPathDomainVerified": true,
      "SPFHost": "string",
      "SPFVerified": true
    }
  ],
  "meta": {}
}
```

See the full [Create Domain action reference](actions/create-domain.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/postmark/latest/actions/create-domain).
