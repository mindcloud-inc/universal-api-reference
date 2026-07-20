# PredictLeads Universal API Examples

These examples use the MindCloud API key and PredictLeads connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Retrieve API Subscription Information

Retrieves API subscription details from the PredictLeads API.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/predictLeads/latest/actions/retrieve-api-subscription-information?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/predictLeads/latest/actions/retrieve-api-subscription-information?${params}`, {
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
  "data": [],
  "meta": {}
}
```

See the full [Retrieve API Subscription Information action reference](actions/retrieve-api-subscription-information.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/predictLeads/latest/actions/retrieve-api-subscription-information).

## Follow Company

Follows a company in the PredictLeads API.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/predictLeads/latest/actions/follow-company" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "companyIdOrDomain": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/predictLeads/latest/actions/follow-company', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "companyIdOrDomain": "string"
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
      "success": {
        "message": "string",
        "type": "string"
      }
    }
  ],
  "meta": {}
}
```

See the full [Follow Company action reference](actions/follow-company.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/predictLeads/latest/actions/follow-company).
