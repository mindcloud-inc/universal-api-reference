# Channels Universal API Examples

These examples use the MindCloud API key and Channels connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Users

Retrieves users from Channels.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/channels/latest/actions/list-users?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/channels/latest/actions/list-users?${params}`, {
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
      "": [
        {
          "doNotAcceptIncomingCalls": true,
          "enabled": true,
          "id": 1,
          "missedIncomingCallsNotification": true,
          "msisdns": [
            "string"
          ],
          "name": "Ava Chen",
          "privatePhoneNumber": "string",
          "role": "string",
          "roleId": 1,
          "state": "string",
          "surname": "Ava Chen",
          "username": "Ava Chen"
        }
      ]
    }
  ],
  "meta": {}
}
```

See the full [List Users action reference](actions/list-users.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/channels/latest/actions/list-users).

## Add Contact Alternative MSISDN

Creates an alternative contact phone number in Channels.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/channels/latest/actions/add-contact-alternative-msisdn" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "contactId": 1,
  "msisdn": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/channels/latest/actions/add-contact-alternative-msisdn', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "contactId": 1,
    "msisdn": "string"
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
      "id": 1,
      "msisdn": "string"
    }
  ],
  "meta": {}
}
```

See the full [Add Contact Alternative MSISDN action reference](actions/add-contact-alternative-msisdn.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/channels/latest/actions/add-contact-alternative-msisdn).
