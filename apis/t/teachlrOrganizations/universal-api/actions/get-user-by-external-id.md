# Teachlr Organizations: Get User By External Id



```
GET https://connect.mindcloud.co/v1/universal/teachlrOrganizations/latest/actions/get-user-by-external-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Teachlr Organizations `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/teachlrOrganizations/latest/actions/get-user-by-external-id?connectionId=$CONNECTION_ID&externalId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "externalId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/teachlrOrganizations/latest/actions/get-user-by-external-id?${params}`, {
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
| `externalId` | string | yes | Teachlr external ID of the user to retrieve. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "alternative_id": "string",
      "certificates": [
        {}
      ],
      "created_at": "string",
      "email": "ava@example.com",
      "employee_number": "string",
      "external_id": "string",
      "groups": [
        {}
      ],
      "id": 1,
      "language": "string",
      "last_name": "Chen",
      "learning": [
        {}
      ],
      "name": "Ava Chen",
      "organization_id": 1,
      "picture": {},
      "register_type": "string",
      "subscriber": true,
      "teaching": [
        {}
      ],
      "username": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `alternative_id` | string |  |
| `certificates` | array<object> |  |
| `created_at` | string |  |
| `email` | string |  |
| `employee_number` | string |  |
| `external_id` | string |  |
| `groups` | array<object> |  |
| `id` | number |  |
| `language` | string |  |
| `last_name` | string |  |
| `learning` | array<object> |  |
| `name` | string |  |
| `organization_id` | number |  |
| `picture` | object |  |
| `register_type` | string |  |
| `subscriber` | boolean |  |
| `teaching` | array<object> |  |
| `username` | string |  |

## Native endpoint

Through the native Teachlr Organizations API, this operation is `GET /users/query` (base URL `https://api.teachlr.com/mindcloudteachlr337933/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-user-by-external-id.md) for the provider-specific parameters and requirements.

