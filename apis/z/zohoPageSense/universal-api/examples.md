# Zoho PageSense Universal API Examples

These examples use the MindCloud API key and Zoho PageSense connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Project Goals

Retrieves project goals from Zoho PageSense.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zohoPageSense/latest/actions/get-project-goals?connectionId=$CONNECTION_ID&portalName=Ava%20Chen&projectLinkname=https%3A%2F%2Fexample.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "portalName": "Ava Chen",
  "projectLinkname": "https://example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zohoPageSense/latest/actions/get-project-goals?${params}`, {
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
      "count": 1,
      "projectgoals": [
        {
          "displayName": "Ava Chen",
          "elementCssSelector": "string",
          "goalStatus": 1,
          "goalType": 1,
          "goalUrl": "https://example.com",
          "linkname": "https://example.com"
        }
      ],
      "statusCode": "string",
      "statusString": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get Project Goals action reference](actions/get-project-goals.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/zohoPageSense/latest/actions/get-project-goals).

## Create Custom Event

Creates a custom event in Zoho PageSense.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/zohoPageSense/latest/actions/create-custom-event" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "portalName": "Ava Chen",
  "customevent.eventName": "Ava Chen",
  "customevent.projectLinkname": "https://example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/zohoPageSense/latest/actions/create-custom-event', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "portalName": "Ava Chen",
    "customevent.eventName": "Ava Chen",
    "customevent.projectLinkname": "https://example.com"
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
      "customevents": [
        {
          "eventId": 1,
          "linkname": "https://example.com",
          "success": true
        }
      ]
    }
  ],
  "meta": {}
}
```

See the full [Create Custom Event action reference](actions/create-custom-event.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/zohoPageSense/latest/actions/create-custom-event).
