# Eventbrite: List Organization Organizers

Retrieves organization organizers from Eventbrite.

```
GET https://connect.mindcloud.co/v1/universal/eventbrite/latest/actions/list-organization-organizers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Eventbrite `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/eventbrite/latest/actions/list-organization-organizers?connectionId=$CONNECTION_ID&organizationId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "organizationId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/eventbrite/latest/actions/list-organization-organizers?${params}`, {
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
| `organizationId` | string | yes | Organization identifier. |

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

Through the native Eventbrite API, this operation is `GET /organizations/:organizationId/organizers/` (base URL `https://www.eventbriteapi.com/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-organization-organizers.md) for the provider-specific parameters and requirements.

