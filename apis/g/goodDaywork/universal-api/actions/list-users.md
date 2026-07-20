# GoodDay.work: List Users

Finds users in the GoodDay.work workspace.

```
GET https://connect.mindcloud.co/v1/universal/goodDaywork/latest/actions/list-users
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GoodDay.work `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/goodDaywork/latest/actions/list-users?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/goodDaywork/latest/actions/list-users?${params}`, {
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
| `deleted` | boolean | no | Set to true to include deleted company users. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "isAdmin": true,
      "name": "Ava Chen",
      "primaryEmail": "ava@example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string | User ID. |
| `isAdmin` | boolean | Whether the user is an administrator. |
| `name` | string | User name. |
| `primaryEmail` | string | Primary email address. |

## Native endpoint

Through the native GoodDay.work API, this operation is `GET /users` (base URL `https://api.goodday.work/2.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-users.md) for the provider-specific parameters and requirements.

