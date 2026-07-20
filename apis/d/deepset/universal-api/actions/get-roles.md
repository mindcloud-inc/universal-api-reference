# Deepset: Get Roles

Retrieves roles for a Deepset organization.

```
GET https://connect.mindcloud.co/v1/universal/deepset/latest/actions/get-roles
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Deepset `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/deepset/latest/actions/get-roles?connectionId=$CONNECTION_ID&limit=25&offset=0&organizationId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "organizationId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/deepset/latest/actions/get-roles?${params}`, {
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
| `organizationId` | string | yes | deepset organization ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        {
          "description": "string",
          "is_custom": true,
          "permissions": [
            {
              "action": "string",
              "asset": "string"
            }
          ],
          "role_id": "string",
          "role_name": "Ava Chen"
        }
      ],
      "has_more": true,
      "total": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data[].description` | string |  |
| `data[].is_custom` | boolean |  |
| `data[].permissions[].action` | string |  |
| `data[].permissions[].asset` | string |  |
| `data[].role_id` | string |  |
| `data[].role_name` | string |  |
| `has_more` | boolean |  |
| `total` | number |  |

## Native endpoint

Through the native Deepset API, this operation is `GET /api/v1/organization/:organization_id/roles` (base URL `https://api.cloud.deepset.ai`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/get-roles.md) for the provider-specific parameters and requirements.

