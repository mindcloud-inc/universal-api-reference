# HIPAAtizer: List All Locations

Retrieves all account locations from HIPAAtizer.

```
GET https://connect.mindcloud.co/v1/universal/hIPAAtizer/latest/actions/list-all-locations
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a HIPAAtizer `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hIPAAtizer/latest/actions/list-all-locations?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hIPAAtizer/latest/actions/list-all-locations?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "address": "string",
      "createdAt": "string",
      "defaultScheduleId": "string",
      "description": "string",
      "email": "ava@example.com",
      "id": "string",
      "isDefault": true,
      "lat": 1,
      "lng": 1,
      "name": "Ava Chen",
      "phone": "string",
      "timeZoneId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `address` | string |  |
| `createdAt` | string |  |
| `defaultScheduleId` | string |  |
| `description` | string |  |
| `email` | string |  |
| `id` | string |  |
| `isDefault` | boolean |  |
| `lat` | number |  |
| `lng` | number |  |
| `name` | string |  |
| `phone` | string |  |
| `timeZoneId` | string |  |

## Native endpoint

Through the native HIPAAtizer API, this operation is `GET /api/v1/api_key/locations/all` (base URL `https://app.hipaatizer.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-all-locations.md) for the provider-specific parameters and requirements.

