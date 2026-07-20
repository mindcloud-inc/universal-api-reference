# Starfish: Create Accommodation

Creates a new accommodation in Starfish.

```
POST https://connect.mindcloud.co/v1/universal/starfish/latest/actions/create-accommodation
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Starfish `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/starfish/latest/actions/create-accommodation" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/starfish/latest/actions/create-accommodation', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | Accommodation name. |

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

Through the native Starfish API, this operation is `POST /accommodations` (base URL `https://api.camping.care/v21`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-accommodation.md) for the provider-specific parameters and requirements.

