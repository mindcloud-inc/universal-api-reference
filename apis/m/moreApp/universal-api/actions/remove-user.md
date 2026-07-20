# MoreApp: Remove User

Removes a user from MoreApp.

```
DELETE https://connect.mindcloud.co/v1/universal/moreApp/latest/actions/remove-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MoreApp `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/moreApp/latest/actions/remove-user?connectionId=$CONNECTION_ID&customerId=1&userId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "customerId": "1",
  "userId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/moreApp/latest/actions/remove-user?${params}`, {
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
| `customerId` | number | yes |  |
| `userId` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "details": {},
      "message": "string",
      "scope": "string",
      "status": 1,
      "traceId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `details` | object |  |
| `message` | string |  |
| `scope` | string |  |
| `status` | number |  |
| `traceId` | string |  |

## Native endpoint

Through the native MoreApp API, this operation is `DELETE /api/v1.0/customers/{{customerId}}/users/{{userId}}` (base URL `https://api.moreapp.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/remove-user.md) for the provider-specific parameters and requirements.

