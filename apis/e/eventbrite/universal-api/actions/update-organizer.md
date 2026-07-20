# Eventbrite: Update Organizer

Updates an existing organizer in Eventbrite.

```
PUT https://connect.mindcloud.co/v1/universal/eventbrite/latest/actions/update-organizer
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Eventbrite `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/eventbrite/latest/actions/update-organizer" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "organizer.name": "Ava Chen",
  "organizerId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/eventbrite/latest/actions/update-organizer', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "organizer.name": "Ava Chen",
    "organizerId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `organizer.name` | string | yes | Updated organizer name. |
| `organizerId` | string | yes | Organizer identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "description": {
        "html": {},
        "text": {}
      },
      "disableMarketingOptIn": true,
      "id": "string",
      "logo": {},
      "logoId": {},
      "longDescription": {
        "html": {},
        "text": {}
      },
      "name": "Ava Chen",
      "numFutureEvents": 1,
      "numPastEvents": 1,
      "organizationId": "string",
      "resourceUri": "string",
      "type": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `description.html` | object |  |
| `description.text` | object |  |
| `disableMarketingOptIn` | boolean |  |
| `id` | string |  |
| `logo` | object |  |
| `logoId` | object |  |
| `longDescription.html` | object |  |
| `longDescription.text` | object |  |
| `name` | string |  |
| `numFutureEvents` | number |  |
| `numPastEvents` | number |  |
| `organizationId` | string |  |
| `resourceUri` | string |  |
| `type` | string |  |
| `url` | string |  |

## Native endpoint

Through the native Eventbrite API, this operation is `POST /organizers/:organizerId/` (base URL `https://www.eventbriteapi.com/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-organizer.md) for the provider-specific parameters and requirements.

