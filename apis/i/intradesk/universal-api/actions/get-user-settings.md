# Intradesk: Get User Settings

Retrieves user settings from Intradesk.

```
GET https://connect.mindcloud.co/v1/universal/intradesk/latest/actions/get-user-settings
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Intradesk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/intradesk/latest/actions/get-user-settings?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/intradesk/latest/actions/get-user-settings?${params}`, {
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
      "email": "ava@example.com",
      "firstName": "Ava",
      "id": 1,
      "lastName": "Chen",
      "middleName": "Ava Chen",
      "name": "Ava Chen",
      "password": "string",
      "phoneNumbers": [
        {}
      ],
      "photoImage": "string",
      "type": 1,
      "userName": "Ava Chen",
      "workingScheduleId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `email` | string |  |
| `firstName` | string |  |
| `id` | number |  |
| `lastName` | string |  |
| `middleName` | string |  |
| `name` | string |  |
| `password` | string |  |
| `phoneNumbers` | array<object> |  |
| `photoImage` | string |  |
| `type` | number |  |
| `userName` | string |  |
| `workingScheduleId` | number |  |

## Native endpoint

Through the native Intradesk API, this operation is `GET /users/api/v1/UserSettings` (base URL `https://apigw.intradesk.ru`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-user-settings.md) for the provider-specific parameters and requirements.

