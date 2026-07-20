# Envoy for Visitors: Get Location

Retrieves a location from Envoy for Visitors.

```
GET https://connect.mindcloud.co/v1/universal/envoyForVisitors/latest/actions/get-location
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Envoy for Visitors `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/envoyForVisitors/latest/actions/get-location?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/envoyForVisitors/latest/actions/get-location?${params}`, {
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
| `id` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "address": {},
      "capacityLimit": 1,
      "companyId": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "enabled": true,
      "id": "string",
      "locale": "string",
      "logoUrl": "https://example.com",
      "name": "Ava Chen",
      "scheduleAheadLimit": 1,
      "timezone": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `address` | object |  |
| `capacityLimit` | number |  |
| `companyId` | string |  |
| `createdAt` | date |  |
| `enabled` | boolean |  |
| `id` | string |  |
| `locale` | string |  |
| `logoUrl` | string |  |
| `name` | string |  |
| `scheduleAheadLimit` | number |  |
| `timezone` | string |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native Envoy for Visitors API, this operation is `GET /locations/:id` (base URL `https://api.envoy.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-location.md) for the provider-specific parameters and requirements.

