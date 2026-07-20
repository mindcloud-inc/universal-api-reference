# RotaCloud: Get Role

Retrieves a role from RotaCloud.

```
GET https://connect.mindcloud.co/v1/universal/rotaCloud/latest/actions/get-role
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a RotaCloud `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rotaCloud/latest/actions/get-role?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rotaCloud/latest/actions/get-role?${params}`, {
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
| `id` | number | yes | The role identifier to retrieve. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "colour": "string",
      "default_break": 1,
      "deleted": true,
      "id": 1,
      "name": "Ava Chen",
      "pay_code": "string",
      "users": [
        1
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `colour` | string |  |
| `default_break` | number |  |
| `deleted` | boolean |  |
| `id` | number |  |
| `name` | string |  |
| `pay_code` | string |  |
| `users` | array<number> |  |

## Native endpoint

Through the native RotaCloud API, this operation is `GET /v1/roles/:id` (base URL `https://api.rotacloud.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-role.md) for the provider-specific parameters and requirements.

