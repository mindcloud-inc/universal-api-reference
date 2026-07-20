# SmartRoutes: Get Vehicle



```
GET https://connect.mindcloud.co/v1/universal/smartRoutes/latest/actions/get-vehicle
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SmartRoutes `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/smartRoutes/latest/actions/get-vehicle?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/smartRoutes/latest/actions/get-vehicle?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | number | yes | ID of the vehicle to retrieve. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "active": true,
      "availability": "string",
      "break": true,
      "capacities": [
        {}
      ],
      "created": "2026-05-07T12:00:00.000Z",
      "endLocation": "string",
      "id": 1,
      "name": "Ava Chen",
      "shift": [
        {}
      ],
      "skills": [
        "string"
      ],
      "startLocation": "string",
      "updated": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `active` | boolean | Whether the vehicle is active. |
| `availability` | string | Vehicle availability mode. |
| `break` | boolean | Whether the vehicle currently has a break configured. |
| `capacities` | array<object> | Vehicle capacities. |
| `created` | date | Vehicle creation timestamp. |
| `endLocation` | string | Vehicle end location type. |
| `id` | number | SmartRoutes vehicle identifier. |
| `name` | string | Vehicle name. |
| `shift` | array<object> | Vehicle shift settings. |
| `skills` | array<string> | Vehicle skills. |
| `startLocation` | string | Vehicle start location type. |
| `updated` | date | Vehicle updated timestamp. |

## Native endpoint

Through the native SmartRoutes API, this operation is `GET /vehicles/:id` (base URL `https://api.smartroutes.io/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-vehicle.md) for the provider-specific parameters and requirements.

