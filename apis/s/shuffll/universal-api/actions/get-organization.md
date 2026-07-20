# Shuffll: Get Organization

Retrieves an organization from Shuffll by ID.

```
GET https://connect.mindcloud.co/v1/universal/shuffll/latest/actions/get-organization
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Shuffll `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/shuffll/latest/actions/get-organization?connectionId=$CONNECTION_ID&organizationId=69cac8104c4a701fd26271a1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "organizationId": "69cac8104c4a701fd26271a1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/shuffll/latest/actions/get-organization?${params}`, {
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
| `organizationId` | string | yes | Shuffll organization id. Default: `69cac8104c4a701fd26271a1`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "branding": {},
      "createdByEmail": "ava@example.com",
      "id": "string",
      "name": "Ava Chen",
      "userCount": 1,
      "workspaces": [
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
| `branding` | object | Organization branding. |
| `createdByEmail` | string | Creator email. |
| `id` | string | Organization id. |
| `name` | string | Organization name. |
| `userCount` | number | Organization user count. |
| `workspaces` | array<object> | Organization workspaces. |

## Native endpoint

Through the native Shuffll API, this operation is `GET /auth/organization/:organizationId` (base URL `https://api.shuffll.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-organization.md) for the provider-specific parameters and requirements.

