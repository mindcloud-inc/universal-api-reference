# Zubie: Update Trip

Updates an existing trip in Zubie.

```
PUT https://connect.mindcloud.co/v1/universal/zubie/latest/actions/update-trip
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zubie `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/zubie/latest/actions/update-trip" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "trip_key": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/zubie/latest/actions/update-trip', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "trip_key": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `trip_key` | string | yes | Unique trip key. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "key": "string",
      "tags": [
        {}
      ],
      "user_key": "string",
      "vehicle_key": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `key` | string |  |
| `tags` | array<object> |  |
| `user_key` | string |  |
| `vehicle_key` | string |  |

## Native endpoint

Through the native Zubie API, this operation is `POST /trip/{trip_key}` (base URL `https://api.zubiecar.com/api/v2/zinc`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-trip.md) for the provider-specific parameters and requirements.

