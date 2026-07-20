# Eventbrite: Get Organizer

Retrieves an organizer from Eventbrite.

```
GET https://connect.mindcloud.co/v1/universal/eventbrite/latest/actions/get-organizer
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Eventbrite `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/eventbrite/latest/actions/get-organizer?connectionId=$CONNECTION_ID&organizerId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "organizerId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/eventbrite/latest/actions/get-organizer?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
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
      "followStatus": {
        "followedAt": {},
        "followedByYou": true,
        "numFollowers": 1
      },
      "id": "string",
      "logo": {},
      "logoId": {},
      "longDescription": {
        "html": {},
        "text": {}
      },
      "name": {},
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
| `followStatus.followedAt` | object |  |
| `followStatus.followedByYou` | boolean |  |
| `followStatus.numFollowers` | number |  |
| `id` | string |  |
| `logo` | object |  |
| `logoId` | object |  |
| `longDescription.html` | object |  |
| `longDescription.text` | object |  |
| `name` | object |  |
| `numFutureEvents` | number |  |
| `numPastEvents` | number |  |
| `organizationId` | string |  |
| `resourceUri` | string |  |
| `type` | string |  |
| `url` | string |  |

## Native endpoint

Through the native Eventbrite API, this operation is `GET /organizers/:organizerId/` (base URL `https://www.eventbriteapi.com/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-organizer.md) for the provider-specific parameters and requirements.

