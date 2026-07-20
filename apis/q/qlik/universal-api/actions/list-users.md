# Qlik: List Users

Retrieves users from your Qlik tenant.

```
GET https://connect.mindcloud.co/v1/universal/qlik/latest/actions/list-users
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Qlik `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/qlik/latest/actions/list-users?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/qlik/latest/actions/list-users?${params}`, {
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
| `filter` | string | no | Optional SCIM filter expression. Example: `email eq "user@example.com"`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        {
          "email": "ava@example.com",
          "id": "string",
          "name": "Ava Chen",
          "status": "string",
          "tenantId": "string"
        }
      ],
      "totalResults": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data[].email` | string |  |
| `data[].id` | string |  |
| `data[].name` | string |  |
| `data[].status` | string |  |
| `data[].tenantId` | string |  |
| `totalResults` | number |  |

## Native endpoint

Through the native Qlik API, this operation is `GET /api/v1/users` (base URL `https://{{credentials.tenantHost}}`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-users.md) for the provider-specific parameters and requirements.

