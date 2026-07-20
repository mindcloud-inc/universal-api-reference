# White Swan: List Account Users

Retrieves account users from White Swan.

```
GET https://connect.mindcloud.co/v1/universal/whiteSwan/latest/actions/list-account-users
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a White Swan `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/whiteSwan/latest/actions/list-account-users?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/whiteSwan/latest/actions/list-account-users?${params}`, {
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
| `userEmail` | string | no | Optionally return one account user by email. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "clients_referred": [
        {}
      ],
      "email": "ava@example.com",
      "name": "Ava Chen",
      "other_partners_referred": [
        {}
      ],
      "permission": "string",
      "total_amount_credited": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `clients_referred` | array<object> |  |
| `email` | string |  |
| `name` | string |  |
| `other_partners_referred` | array<object> |  |
| `permission` | string |  |
| `total_amount_credited` | number |  |

## Native endpoint

Through the native White Swan API, this operation is `POST /user` (base URL `https://app.whiteswan.io/api/1.1/wf`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-account-users.md) for the provider-specific parameters and requirements.

