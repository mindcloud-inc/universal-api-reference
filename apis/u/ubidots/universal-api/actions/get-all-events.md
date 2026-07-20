# Ubidots: Get all Events



```
GET https://connect.mindcloud.co/v1/universal/ubidots/latest/actions/get-all-events
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ubidots `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ubidots/latest/actions/get-all-events?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ubidots/latest/actions/get-all-events?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "action": {},
      "activeDates": {},
      "createdAt": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "id": "string",
      "isActive": true,
      "label": "string",
      "name": "Ava Chen",
      "trigger": {},
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `action` | object |  |
| `activeDates` | object |  |
| `createdAt` | date |  |
| `description` | string |  |
| `id` | string |  |
| `isActive` | boolean |  |
| `label` | string |  |
| `name` | string |  |
| `trigger` | object |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native Ubidots API, this operation is `GET /events/` (base URL `https://industrial.api.ubidots.com/api/v2.0`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/get-all-events.md) for the provider-specific parameters and requirements.

