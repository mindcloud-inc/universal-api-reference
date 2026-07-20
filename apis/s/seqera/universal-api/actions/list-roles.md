# Seqera: List Roles

Retrieves available roles from Seqera.

```
GET https://connect.mindcloud.co/v1/universal/seqera/latest/actions/list-roles
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Seqera `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/seqera/latest/actions/list-roles?connectionId=$CONNECTION_ID&limit=25&offset=0&orgId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "orgId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/seqera/latest/actions/list-roles?${params}`, {
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
| `orgId` | number | yes |  |
| `limit` | number | no | Maximum number of roles to return. |
| `offset` | number | no | Number of roles to skip before returning results. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "roles": [
        {
          "description": "string",
          "isPredefined": true,
          "name": "Ava Chen"
        }
      ],
      "totalSize": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `roles` | array<object> | Available roles. |
| `roles[].description` | string | Role description. |
| `roles[].isPredefined` | boolean | Whether the role is predefined. |
| `roles[].name` | string | Role name. |
| `totalSize` | number | Total number of roles returned. |

## Native endpoint

Through the native Seqera API, this operation is `GET /roles` (base URL `https://api.cloud.seqera.io`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-roles.md) for the provider-specific parameters and requirements.

