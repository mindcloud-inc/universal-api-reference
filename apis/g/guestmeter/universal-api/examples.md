# Guestmeter Universal API Examples

These examples use the MindCloud API key and Guestmeter connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Guests

Retrieves guests from Guestmeter.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/guestmeter/latest/actions/list-guests?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/guestmeter/latest/actions/list-guests?${params}`, {
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
      "clickedDate": "string",
      "contactInfo": "string",
      "contactType": "string",
      "countryCode": "string",
      "creationDate": "string",
      "feedback": "string",
      "guestID": "string",
      "guestName": "Ava Chen",
      "integrationID": "string",
      "languageCode": "string",
      "mainChannel": "string",
      "propertyName": "Ava Chen",
      "ratedDate": "string",
      "rating": "string",
      "ratingType": "string",
      "roomNumber": "string",
      "sentDate": "string",
      "status": "string",
      "statusDetail": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Guests action reference](actions/list-guests.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/guestmeter/latest/actions/list-guests).

## Send Survey

Creates a guest survey request in Guestmeter.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/guestmeter/latest/actions/send-survey" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "guestEmail": "guest@example.com",
  "guestName": "Jane Guest"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/guestmeter/latest/actions/send-survey', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "guestEmail": "guest@example.com",
    "guestName": "Jane Guest"
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
      "statusList": [
        {
          "status": "string",
          "statusCode": "string",
          "statusMessage": "string"
        }
      ]
    }
  ],
  "meta": {}
}
```

See the full [Send Survey action reference](actions/send-survey.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/guestmeter/latest/actions/send-survey).
