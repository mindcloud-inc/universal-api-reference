# SendPulse Universal API Examples

These examples use the MindCloud API key and SendPulse connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Account Information

Retrieves account profile information from SendPulse.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sendPulse/latest/actions/get-account-information?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sendPulse/latest/actions/get-account-information?${params}`, {
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
      "avatar": "string",
      "city": "string",
      "country": "string",
      "currency": "string",
      "email": "ava@example.com",
      "first_name": "Ava",
      "id": 1,
      "lang": "string",
      "last_name": "Chen",
      "locale": "string",
      "name": "Ava Chen",
      "phone": "string",
      "phone_confirm": true,
      "time_zone": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get Account Information action reference](actions/get-account-information.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/sendPulse/latest/actions/get-account-information).

## Add Emails to Mailing List

Creates subscribers in a SendPulse mailing list.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/sendPulse/latest/actions/add-emails-to-mailing-list" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "mailingListId": "123456",
  "emails[]": "user@example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/sendPulse/latest/actions/add-emails-to-mailing-list', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "mailingListId": "123456",
    "emails[]": "user@example.com"
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
      "result": true
    }
  ],
  "meta": {}
}
```

See the full [Add Emails to Mailing List action reference](actions/add-emails-to-mailing-list.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/sendPulse/latest/actions/add-emails-to-mailing-list).
