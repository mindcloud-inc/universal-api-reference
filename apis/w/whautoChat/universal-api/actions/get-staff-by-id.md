# WhautoChat: Get Staff by ID

Retrieves a staff member from WhautoChat by ID.

```
GET https://connect.mindcloud.co/v1/universal/whautoChat/latest/actions/get-staff-by-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a WhautoChat `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/whautoChat/latest/actions/get-staff-by-id?connectionId=$CONNECTION_ID&staffId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "staffId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/whautoChat/latest/actions/get-staff-by-id?${params}`, {
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
| `staffId` | string | yes | Staff unique ID |

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
      "phone": "string",
      "workspaces": [
        "string"
      ]
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
| `phone` | string |  |
| `workspaces` | array<string> |  |

## Native endpoint

Through the native WhautoChat API, this operation is `GET /v1/staffs/{staffId}` (base URL `https://api.whauto.chat`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-staff-by-id.md) for the provider-specific parameters and requirements.

