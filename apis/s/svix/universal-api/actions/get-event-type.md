# Svix: Get Event Type

Retrieves an event type from Svix.

```
GET https://connect.mindcloud.co/v1/universal/svix/latest/actions/get-event-type
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Svix `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/svix/latest/actions/get-event-type?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/svix/latest/actions/get-event-type?${params}`, {
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
      "archived": true,
      "createdAt": "string",
      "deprecated": true,
      "description": "string",
      "featureFlag": "string",
      "featureFlags": [
        "string"
      ],
      "groupName": "Ava Chen",
      "name": "Ava Chen",
      "schemas": {},
      "updatedAt": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `archived` | boolean |  |
| `createdAt` | string |  |
| `deprecated` | boolean |  |
| `description` | string |  |
| `featureFlag` | string |  |
| `featureFlags` | array<string> |  |
| `groupName` | string |  |
| `name` | string |  |
| `schemas` | object |  |
| `updatedAt` | string |  |

## Native endpoint

Through the native Svix API, this operation is `GET /api/v1/event-type/{event_type_name}` (base URL `https://api.us.svix.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-event-type.md) for the provider-specific parameters and requirements.

