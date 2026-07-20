# ChurchStamp Universal API Examples

These examples use the MindCloud API key and ChurchStamp connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get User Details

Retrieves authenticated user details from ChurchStamp.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/churchStamp/latest/actions/get-user-details?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/churchStamp/latest/actions/get-user-details?${params}`, {
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
      "creditsBalance": {},
      "emailAddress": "ava@example.com",
      "firstName": "Ava",
      "lastName": "Chen",
      "subscriptionPlan": "string",
      "subscriptionStatus": "string",
      "vAddress": {}
    }
  ],
  "meta": {}
}
```

See the full [Get User Details action reference](actions/get-user-details.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/churchStamp/latest/actions/get-user-details).

## Send Mail

Sends campaign mail to a recipient in ChurchStamp.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/churchStamp/latest/actions/send-mail" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "campaignId": "1731535111267x707091876624990200",
  "firstName": "John",
  "lastName": "Doe",
  "email": "john@example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/churchStamp/latest/actions/send-mail', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "campaignId": "1731535111267x707091876624990200",
    "firstName": "John",
    "lastName": "Doe",
    "email": "john@example.com"
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
      "campaign_id": "string",
      "Created By": "string",
      "Created Date": 1,
      "email": "ava@example.com",
      "mail_id": "string"
    }
  ],
  "meta": {}
}
```

See the full [Send Mail action reference](actions/send-mail.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/churchStamp/latest/actions/send-mail).
