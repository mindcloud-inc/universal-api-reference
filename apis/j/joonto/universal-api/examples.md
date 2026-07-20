# Joonto Universal API Examples

These examples use the MindCloud API key and Joonto connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List SMS Contacts



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/joonto/latest/actions/list-sms-contacts?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/joonto/latest/actions/list-sms-contacts?${params}`, {
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
      "active": true,
      "billingCycle": "string",
      "companyName": "Ava Chen",
      "count": 1,
      "dateCreated": "2026-05-07T12:00:00.000Z",
      "email": "ava@example.com",
      "id": 1,
      "imageId": 1,
      "joontoPhone": "string",
      "joontoPhonePretty": "string",
      "locked": true,
      "name": "Ava Chen",
      "phone": "string",
      "phonePretty": "string",
      "phoneVerified": true,
      "plan": "string",
      "timeZone": "string",
      "timeZoneFriendly": "string",
      "timeZoneHours": 1,
      "timeZoneHoursAdd": 1,
      "userManagerStatus": "string"
    }
  ],
  "meta": {}
}
```

See the full [List SMS Contacts action reference](actions/list-sms-contacts.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/joonto/latest/actions/list-sms-contacts).
