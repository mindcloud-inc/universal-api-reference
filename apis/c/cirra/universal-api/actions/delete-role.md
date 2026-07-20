# Cirra: Delete Role

Deletes a role from Cirra by role ID.

```
DELETE https://connect.mindcloud.co/v1/universal/cirra/latest/actions/delete-role
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cirra `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/cirra/latest/actions/delete-role?connectionId=$CONNECTION_ID&roleId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "roleId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cirra/latest/actions/delete-role?${params}`, {
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
| `roleId` | list | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "companyId": "string",
      "description": "string",
      "id": "string",
      "isBuiltIn": true,
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `companyId` | string |  |
| `description` | string |  |
| `id` | string |  |
| `isBuiltIn` | boolean |  |
| `name` | string |  |

## Native endpoint

Through the native Cirra API, this operation is `DELETE /v1/cirra/roles/:roleId` (base URL `http://api-public:9801`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-role.md) for the provider-specific parameters and requirements.

