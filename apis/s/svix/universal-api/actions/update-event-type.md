# Svix: Update Event Type

Updates an event type in Svix.

```
PUT https://connect.mindcloud.co/v1/universal/svix/latest/actions/update-event-type
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Svix `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/svix/latest/actions/update-event-type" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/svix/latest/actions/update-event-type', {
  method: 'PUT',
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

Through the native Svix API, this operation is `PUT /api/v1/event-type/{event_type_name}` (base URL `https://api.us.svix.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-event-type.md) for the provider-specific parameters and requirements.

