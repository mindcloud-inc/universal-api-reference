# Heymarket SMS: Get Users



```
GET https://connect.mindcloud.co/v1/universal/heymarketSMS/latest/actions/get-users
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Heymarket SMS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/heymarketSMS/latest/actions/get-users?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/heymarketSMS/latest/actions/get-users?${params}`, {
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
| `phone[]` | array<string> | no | Phone numbers of users to search for within the team. |
| `email[]` | array<string> | no | Email addresses of users to search for within the team. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "memberships": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `memberships` | array<object> |  |

## Native endpoint

Through the native Heymarket SMS API, this operation is `GET /v1/users/get` (base URL `https://api.heymarket.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-users.md) for the provider-specific parameters and requirements.

