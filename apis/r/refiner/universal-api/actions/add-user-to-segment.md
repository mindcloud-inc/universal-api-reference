# Refiner: Add User to Segment

Adds a user to a manual segment in Refiner.

```
POST https://connect.mindcloud.co/v1/universal/refiner/latest/actions/add-user-to-segment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Refiner `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/refiner/latest/actions/add-user-to-segment" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "segmentUuid": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/refiner/latest/actions/add-user-to-segment', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "segmentUuid": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | no | Identify the user by your own user ID. |
| `email` | string | no | Identify the user by email address. |
| `segmentUuid` | string | yes | The manual segment UUID to add the user to. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "contactUuid": "string",
      "message": "string",
      "segmentUid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `contactUuid` | string |  |
| `message` | string |  |
| `segmentUid` | string |  |

## Native endpoint

Through the native Refiner API, this operation is `POST /sync-segment` (base URL `https://api.refiner.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-user-to-segment.md) for the provider-specific parameters and requirements.

