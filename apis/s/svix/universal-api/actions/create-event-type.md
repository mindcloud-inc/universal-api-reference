# Svix: Create Event Type

Creates or unarchives an event type in Svix.

```
POST https://connect.mindcloud.co/v1/universal/svix/latest/actions/create-event-type
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Svix `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/svix/latest/actions/create-event-type" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/svix/latest/actions/create-event-type', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
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

Through the native Svix API, this operation is `POST /api/v1/event-type` (base URL `https://api.us.svix.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-event-type.md) for the provider-specific parameters and requirements.

