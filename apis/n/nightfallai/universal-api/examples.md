# Nightfall.ai Universal API Examples

These examples use the MindCloud API key and Nightfall.ai connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Violations

Retrieves violations from Nightfall.ai.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/nightfallai/latest/actions/list-violations?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/nightfallai/latest/actions/list-violations?${params}`, {
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
      "violations": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

See the full [List Violations action reference](actions/list-violations.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/nightfallai/latest/actions/list-violations).

## Annotate Finding

Updates a finding annotation in Nightfall.ai.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/nightfallai/latest/actions/annotate-finding" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "findingId": "string",
  "type": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/nightfallai/latest/actions/annotate-finding', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "findingId": "string",
    "type": "string"
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

See the full [Annotate Finding action reference](actions/annotate-finding.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/nightfallai/latest/actions/annotate-finding).
