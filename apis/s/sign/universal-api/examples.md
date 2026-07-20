# Sign Universal API Examples

These examples use the MindCloud API key and Sign connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get all templates

Retrieves templates from CM.com Sign.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sign/latest/actions/get-all-templates?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sign/latest/actions/get-all-templates?${params}`, {
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
      "currentPage": 1,
      "data": [
        {}
      ],
      "from": 1,
      "lastPage": 1,
      "perPage": 1,
      "to": 1,
      "total": 1
    }
  ],
  "meta": {}
}
```

See the full [Get all templates action reference](actions/get-all-templates.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/sign/latest/actions/get-all-templates).

## Add webhook

Creates a webhook in CM.com Sign.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/sign/latest/actions/add-webhook" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/sign/latest/actions/add-webhook', {
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
  "data": [],
  "meta": {}
}
```

See the full [Add webhook action reference](actions/add-webhook.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/sign/latest/actions/add-webhook).
