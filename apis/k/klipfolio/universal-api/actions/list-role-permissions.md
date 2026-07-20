# Klipfolio: List Role Permissions

Retrieves permissions for a Klipfolio role.

```
GET https://connect.mindcloud.co/v1/universal/klipfolio/latest/actions/list-role-permissions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Klipfolio `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/klipfolio/latest/actions/list-role-permissions?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/klipfolio/latest/actions/list-role-permissions?${params}`, {
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
| `roleId` | string | no | The Klipfolio role ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "permissions": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `permissions` | array<string> |  |

## Native endpoint

Through the native Klipfolio API, this operation is `GET /roles/:roleId/permissions` (base URL `https://app.klipfolio.com/api/1.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-role-permissions.md) for the provider-specific parameters and requirements.

