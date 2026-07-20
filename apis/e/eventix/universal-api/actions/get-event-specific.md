# Eventix: Get a specific Event

Retrieves a specific event from Eventix.

```
GET https://connect.mindcloud.co/v1/universal/eventix/latest/actions/get-event-specific
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Eventix `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/eventix/latest/actions/get-event-specific?connectionId=$CONNECTION_ID&guid=event-guid" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "guid": "event-guid"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/eventix/latest/actions/get-event-specific?${params}`, {
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
| `guid` | string | yes | The guid of the Event. Example: `event-guid`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "auto-prune": true,
      "category": "string",
      "company_id": "string",
      "currency": "string",
      "description": "string",
      "guid": "string",
      "locale": "string",
      "location": {},
      "location_id": "string",
      "name": "Ava Chen",
      "retrievable_after": "2026-05-07T12:00:00.000Z",
      "status": "string",
      "subcategories": [
        "string"
      ],
      "type": "string",
      "website": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `auto-prune` | boolean |  |
| `category` | string |  |
| `company_id` | string |  |
| `currency` | string |  |
| `description` | string |  |
| `guid` | string |  |
| `locale` | string |  |
| `location` | object |  |
| `location_id` | string |  |
| `name` | string |  |
| `retrievable_after` | date |  |
| `status` | string |  |
| `subcategories` | array<string> |  |
| `type` | string |  |
| `website` | string |  |

## Native endpoint

Through the native Eventix API, this operation is `GET /3.0.0/event/:guid` (base URL `https://api.weeztix.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-event-specific.md) for the provider-specific parameters and requirements.

