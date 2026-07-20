# MailerSend Universal API Examples

These examples use the MindCloud API key and MailerSend connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Messages



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mailerSend/latest/actions/list-messages?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mailerSend/latest/actions/list-messages?${params}`, {
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
      "createdAt": "string",
      "id": "string",
      "updatedAt": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Messages action reference](actions/list-messages.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/mailerSend/latest/actions/list-messages).

## Add Domain



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/mailerSend/latest/actions/add-domain" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/mailerSend/latest/actions/add-domain', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen"
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
      "can": {},
      "dkim": true,
      "domainSettings": {},
      "id": "string",
      "isBeingVerified": true,
      "isCustomLinksAvailable": true,
      "isDnsActive": true,
      "isTrialDomain": true,
      "isVerified": true,
      "name": "Ava Chen",
      "showDkimInfo": true,
      "spf": true,
      "totals": [
        {}
      ],
      "tracking": true
    }
  ],
  "meta": {}
}
```

See the full [Add Domain action reference](actions/add-domain.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/mailerSend/latest/actions/add-domain).
