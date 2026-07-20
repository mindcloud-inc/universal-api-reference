# Whautomate: Get Staff

Retrieves a staff member from Whautomate.

```
GET https://connect.mindcloud.co/v1/universal/whautomate/latest/actions/get-staff
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Whautomate `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/whautomate/latest/actions/get-staff?connectionId=$CONNECTION_ID&staffId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "staffId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/whautomate/latest/actions/get-staff?${params}`, {
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
| `staffId` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "active": true,
      "countryCode": "string",
      "email": "ava@example.com",
      "firstName": "Ava",
      "id": "string",
      "lastName": "Chen",
      "locations": [
        "string"
      ],
      "phone": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `active` | boolean |  |
| `countryCode` | string |  |
| `email` | string |  |
| `firstName` | string |  |
| `id` | string |  |
| `lastName` | string |  |
| `locations` | array<string> |  |
| `phone` | string |  |

## Native endpoint

Through the native Whautomate API, this operation is `GET /v1/staffs/{{staffId}}` (base URL `https://api.whautomate.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-staff.md) for the provider-specific parameters and requirements.

