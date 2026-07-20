# Zoho PageSense: Create Custom Event

Creates a custom event in Zoho PageSense.

```
POST https://connect.mindcloud.co/v1/universal/zohoPageSense/latest/actions/create-custom-event
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho PageSense `connectionId` ([setup](../authentication.md)).

## Example request

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

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `portalName` | string | yes | Portal identifier in the path. |
| `customevent.eventName` | string | yes | Human-friendly custom event name. |
| `customevent.projectLinkname` | string | yes | Project linkname for the custom event. |

## Response

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

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `customevents[].eventId` | number |  |
| `customevents[].linkname` | string |  |
| `customevents[].success` | boolean |  |

## Native endpoint

Through the native Zoho PageSense API, this operation is `POST /portal/:portalName/customevents` (base URL `https://pagesense.zoho.com/pagesense/rest/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-custom-event.md) for the provider-specific parameters and requirements.

