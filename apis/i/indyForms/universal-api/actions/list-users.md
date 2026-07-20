# IndyForms: List Users



```
GET https://connect.mindcloud.co/v1/universal/indyForms/latest/actions/list-users
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a IndyForms `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/indyForms/latest/actions/list-users?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/indyForms/latest/actions/list-users?${params}`, {
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
| `includeDeactivated` | boolean | no |  |
| `status` | number | no |  |
| `keywords` | string | no |  |
| `rangeStart` | number | no |  |
| `rangeEnd` | number | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "dateCreated": "2026-05-07T12:00:00.000Z",
      "email": "ava@example.com",
      "firstName": "Ava",
      "fullName": "Ava Chen",
      "id": "string",
      "lastName": "Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `dateCreated` | date |  |
| `email` | string |  |
| `firstName` | string |  |
| `fullName` | string |  |
| `id` | string |  |
| `lastName` | string |  |

## Native endpoint

Through the native IndyForms API, this operation is `GET /api/public/v2/users` (base URL `https://api.indyforms.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-users.md) for the provider-specific parameters and requirements.

