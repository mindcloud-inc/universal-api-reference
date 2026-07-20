# Eventix: Get Events

Retrieves events from Eventix.

```
GET https://connect.mindcloud.co/v1/universal/eventix/latest/actions/get-events
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Eventix `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/eventix/latest/actions/get-events?connectionId=$CONNECTION_ID&type=normal" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "type": "normal"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/eventix/latest/actions/get-events?${params}`, {
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
| `type` | list<string> | yes | How to handle archived or dated events. Use normal for active events, past for past events, and upcoming for future events. One of: `0`, `1`, `2`, `3`, `4`. Default: `normal`. Example: `normal`. |

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

Through the native Eventix API, this operation is `GET /3.0.0/event/:type` (base URL `https://api.weeztix.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-events.md) for the provider-specific parameters and requirements.

