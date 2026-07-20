# Eventbrite: Create Organization Organizer

Creates a new organization organizer in Eventbrite.

```
POST https://connect.mindcloud.co/v1/universal/eventbrite/latest/actions/create-organization-organizer
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Eventbrite `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/eventbrite/latest/actions/create-organization-organizer" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "organizationId": "string",
  "organizer.name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/eventbrite/latest/actions/create-organization-organizer', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "organizationId": "string",
    "organizer.name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `organizationId` | string | yes | Organization identifier. |
| `organizer.name` | string | yes | Organizer display name. |

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

Through the native Eventbrite API, this operation is `POST /organizations/:organizationId/organizers/` (base URL `https://www.eventbriteapi.com/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-organization-organizer.md) for the provider-specific parameters and requirements.

