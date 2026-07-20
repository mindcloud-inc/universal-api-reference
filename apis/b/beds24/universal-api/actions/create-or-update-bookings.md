# Beds24: Create or Update Bookings

Creates or updates bookings in Beds24.

```
POST https://connect.mindcloud.co/v1/universal/beds24/latest/actions/create-or-update-bookings
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Beds24 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/beds24/latest/actions/create-or-update-bookings" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/beds24/latest/actions/create-or-update-bookings', {
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
      "errors": [
        {}
      ],
      "info": [
        {}
      ],
      "modified": {},
      "new": {},
      "success": true,
      "warnings": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `errors` | array<object> |  |
| `info` | array<object> |  |
| `modified` | object |  |
| `new` | object |  |
| `success` | boolean |  |
| `warnings` | array<object> |  |

## Native endpoint

Through the native Beds24 API, this operation is `POST /bookings` (base URL `https://beds24.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-or-update-bookings.md) for the provider-specific parameters and requirements.

