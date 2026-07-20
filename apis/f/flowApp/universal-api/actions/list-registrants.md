# Flow App: List Registrants



```
GET https://connect.mindcloud.co/v1/universal/flowApp/latest/actions/list-registrants
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Flow App `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/flowApp/latest/actions/list-registrants?connectionId=$CONNECTION_ID&sessionToken=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "sessionToken": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/flowApp/latest/actions/list-registrants?${params}`, {
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
| `sessionToken` | string | yes | The event session token whose registrants you want to list. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "camEnabled": 1,
      "email": "ava@example.com",
      "entryTime": "string",
      "eventSessionID": 1,
      "exitTime": "string",
      "firstName": "Ava",
      "lastName": "Chen",
      "location": "string",
      "micEnabled": 1,
      "phone": "string",
      "role": 1,
      "screenSharingEnabled": 1,
      "token": "string",
      "userID": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `camEnabled` | number |  |
| `email` | string |  |
| `entryTime` | string |  |
| `eventSessionID` | number |  |
| `exitTime` | string |  |
| `firstName` | string |  |
| `lastName` | string |  |
| `location` | string |  |
| `micEnabled` | number |  |
| `phone` | string |  |
| `role` | number |  |
| `screenSharingEnabled` | number |  |
| `token` | string |  |
| `userID` | number |  |

## Native endpoint

Through the native Flow App API, this operation is `GET /reports/events/sessions/registrants/:sessionToken` (base URL `https://prod.flowapp.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-registrants.md) for the provider-specific parameters and requirements.

