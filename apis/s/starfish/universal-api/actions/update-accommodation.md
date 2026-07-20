# Starfish: Update Accommodation

Updates an existing accommodation in Starfish.

```
PUT https://connect.mindcloud.co/v1/universal/starfish/latest/actions/update-accommodation
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Starfish `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/starfish/latest/actions/update-accommodation" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "accommodationId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/starfish/latest/actions/update-accommodation', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "accommodationId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `accommodationId` | number | yes | Accommodation ID. |
| `name` | string | no | Updated accommodation name. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accommodationId": 1,
      "accommodationUid": "string",
      "adminId": 1,
      "arrangements": [
        {}
      ],
      "description": "string",
      "id": 1,
      "labels": [
        {}
      ],
      "media": [
        {}
      ],
      "meta": {},
      "name": "Ava Chen",
      "rank": 1,
      "services": [
        {}
      ],
      "status": "string",
      "translations": [
        {}
      ],
      "type": "string",
      "vatProcent": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accommodationId` | number |  |
| `accommodationUid` | string |  |
| `adminId` | number |  |
| `arrangements` | array<object> |  |
| `description` | string |  |
| `id` | number |  |
| `labels` | array<object> |  |
| `media` | array<object> |  |
| `meta` | object |  |
| `name` | string |  |
| `rank` | number |  |
| `services` | array<object> |  |
| `status` | string |  |
| `translations` | array<object> |  |
| `type` | string |  |
| `vatProcent` | number |  |

## Native endpoint

Through the native Starfish API, this operation is `PUT /accommodations/:accommodation_id` (base URL `https://api.camping.care/v21`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-accommodation.md) for the provider-specific parameters and requirements.

