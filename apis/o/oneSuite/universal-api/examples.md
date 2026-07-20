# OneSuite Universal API Examples

These examples use the MindCloud API key and OneSuite connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Opportunity Stages

Retrieves opportunity stages from OneSuite.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/oneSuite/latest/actions/get-opportunity-stages?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/oneSuite/latest/actions/get-opportunity-stages?${params}`, {
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
      "bgColor": "string",
      "borderColor": "string",
      "businessId": "string",
      "createdAt": "string",
      "darkColor": "string",
      "fgColor": "string",
      "id": "string",
      "isDefault": true,
      "isFolded": true,
      "lightColor": "string",
      "name": "Ava Chen",
      "sortId": 1,
      "updatedAt": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get Opportunity Stages action reference](actions/get-opportunity-stages.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/oneSuite/latest/actions/get-opportunity-stages).

## Connect Opportunity to Company

Connects an opportunity to a company in OneSuite.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/oneSuite/latest/actions/connect-opportunity-to-company" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "opportunityId": "cmo7h1vjm02stbo05mhgr2rmy",
  "companyId": "cmo7gzxna02smbo056u59sb9y"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/oneSuite/latest/actions/connect-opportunity-to-company', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "opportunityId": "cmo7h1vjm02stbo05mhgr2rmy",
    "companyId": "cmo7gzxna02smbo056u59sb9y"
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

See the full [Connect Opportunity to Company action reference](actions/connect-opportunity-to-company.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/oneSuite/latest/actions/connect-opportunity-to-company).
