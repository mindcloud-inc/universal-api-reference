# Xola Universal API Examples

These examples use the MindCloud API key and Xola connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Experiences

Finds experiences in Xola.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/xola/latest/actions/list-experiences?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/xola/latest/actions/list-experiences?${params}`, {
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
      "autoChargeOnDepositReminder": true,
      "balanceDueOffset": 1,
      "balanceDueReminder": true,
      "businessHours": "string",
      "category": "string",
      "complete": true,
      "currency": "string",
      "customerNamePreference": "Ava Chen",
      "cutoff": 1,
      "desc": "string",
      "duration": 1,
      "earlyReturn": true,
      "eventDuration": 1,
      "excerpt": "string",
      "geo": {
        "lat": 1,
        "lng": 1
      },
      "group": {
        "orderMax": 1,
        "orderMin": 1,
        "outingMax": 1,
        "outingMin": 1,
        "outingMinCutoff": 1
      },
      "guestType": "string",
      "id": "string",
      "isScheduled": true,
      "name": "Ava Chen",
      "paymentMethod": "string",
      "photo": {
        "id": "string",
        "src": "string",
        "type": "string"
      },
      "pickupAddress": "string",
      "pickupGeo": {
        "lat": 1,
        "lng": 1
      },
      "requireAdult": true,
      "requireGuestIdentification": true,
      "scheduleType": "string",
      "seller": {
        "id": "string"
      },
      "status": "string",
      "travelerPreference": {
        "allowPayment": {
          "value": true
        },
        "questionnaire": {
          "value": true
        }
      },
      "updated": "2026-05-07T12:00:00.000Z",
      "visible": true
    }
  ],
  "meta": {}
}
```

See the full [List Experiences action reference](actions/list-experiences.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/xola/latest/actions/list-experiences).

## Create Affiliate

Creates a new affiliate for a seller in Xola.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/xola/latest/actions/create-affiliate" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "code": "string",
  "id": "string",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/xola/latest/actions/create-affiliate', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "code": "string",
    "id": "string",
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
      "id": "string",
      "name": "Ava Chen",
      "object": "string",
      "seller": {
        "id": "string"
      }
    }
  ],
  "meta": {}
}
```

See the full [Create Affiliate action reference](actions/create-affiliate.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/xola/latest/actions/create-affiliate).
