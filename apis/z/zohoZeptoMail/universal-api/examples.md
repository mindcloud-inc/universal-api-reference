# Zoho ZeptoMail Universal API Examples

These examples use the MindCloud API key and Zoho ZeptoMail connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Download Export

Downloads a log export from Zoho ZeptoMail.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zohoZeptoMail/latest/actions/download-export?connectionId=$CONNECTION_ID&exportType=string&exportId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "exportType": "string",
  "exportId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zohoZeptoMail/latest/actions/download-export?${params}`, {
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
      "content": "string"
    }
  ],
  "meta": {}
}
```

See the full [Download Export action reference](actions/download-export.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/zohoZeptoMail/latest/actions/download-export).

## Add Domain

Adds a new domain in Zoho ZeptoMail.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/zohoZeptoMail/latest/actions/add-domain" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "domainName": "Ava Chen",
  "subDomainPrefix": "string",
  "mailagent_keys[0]": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/zohoZeptoMail/latest/actions/add-domain', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "domainName": "Ava Chen",
    "subDomainPrefix": "string",
    "mailagent_keys[0]": "string"
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
      "data": {
        "domain_key": "string",
        "domain_name": "Ava Chen",
        "mailagent_keys": [
          "string"
        ],
        "status": "string",
        "sub_domain_prefix": "string",
        "verified": true
      }
    }
  ],
  "meta": {}
}
```

See the full [Add Domain action reference](actions/add-domain.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/zohoZeptoMail/latest/actions/add-domain).
