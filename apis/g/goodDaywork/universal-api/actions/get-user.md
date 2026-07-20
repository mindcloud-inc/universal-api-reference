# GoodDay.work: Get User

Retrieves a single user from GoodDay.work.

```
GET https://connect.mindcloud.co/v1/universal/goodDaywork/latest/actions/get-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GoodDay.work `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/goodDaywork/latest/actions/get-user?connectionId=$CONNECTION_ID&userId=Hn7mvN" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "userId": "Hn7mvN"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/goodDaywork/latest/actions/get-user?${params}`, {
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
| `userId` | string | yes | GoodDay user ID. Default: `Hn7mvN`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "companyRole": 1,
      "departmentId": "string",
      "id": "string",
      "isAdmin": true,
      "momentCreated": "string",
      "name": "Ava Chen",
      "phoneNumber": "string",
      "primaryEmail": "ava@example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `companyRole` | number | Company role value. |
| `departmentId` | string | Department ID. |
| `id` | string | User ID. |
| `isAdmin` | boolean | Whether the user is an administrator. |
| `momentCreated` | string | Creation timestamp. |
| `name` | string | User full name. |
| `phoneNumber` | string | Phone number. |
| `primaryEmail` | string | Primary email address. |

## Native endpoint

Through the native GoodDay.work API, this operation is `GET /user/:userId` (base URL `https://api.goodday.work/2.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-user.md) for the provider-specific parameters and requirements.

