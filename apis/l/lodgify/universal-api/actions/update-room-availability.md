# Lodgify: Update Room Availability

Updates a room's availability in Lodgify.

```
PUT https://connect.mindcloud.co/v1/universal/lodgify/latest/actions/update-room-availability
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Lodgify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/lodgify/latest/actions/update-room-availability" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "propertyId": 1,
  "roomTypeId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/lodgify/latest/actions/update-room-availability', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "propertyId": 1,
    "roomTypeId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `propertyId` | number | yes |  |
| `roomTypeId` | number | yes |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Lodgify API returns.

## Native endpoint

Through the native Lodgify API, this operation is `POST /v1/availability/:propertyId/:roomTypeId/set` (base URL `https://api.lodgify.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-room-availability.md) for the provider-specific parameters and requirements.

