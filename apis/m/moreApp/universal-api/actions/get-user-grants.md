# MoreApp: Get User Grants

Retrieves a user's grants from MoreApp.

```
GET https://connect.mindcloud.co/v1/universal/moreApp/latest/actions/get-user-grants
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MoreApp `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/moreApp/latest/actions/get-user-grants?connectionId=$CONNECTION_ID&customerId=1&userId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "customerId": "1",
  "userId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/moreApp/latest/actions/get-user-grants?${params}`, {
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
      "customerId": 1,
      "resourceId": "string",
      "resourceType": "string",
      "roleId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `customerId` | number |  |
| `resourceId` | string |  |
| `resourceType` | string |  |
| `roleId` | string |  |

## Native endpoint

Through the native MoreApp API, this operation is `GET /api/v2/customers/{{customerId}}/users/{{userId}}/grants` (base URL `https://api.moreapp.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-user-grants.md) for the provider-specific parameters and requirements.

