# Starburst Galaxy: Get role



```
GET https://connect.mindcloud.co/v1/universal/starburstGalaxy/latest/actions/get-role
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Starburst Galaxy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/starburstGalaxy/latest/actions/get-role?connectionId=$CONNECTION_ID&roleId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "roleId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/starburstGalaxy/latest/actions/get-role?${params}`, {
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
| `roleId` | string | yes | Starburst Galaxy role ID. Docs also support URL-encoded lookup expressions such as name=value. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdOn": "2026-05-07T12:00:00.000Z",
      "modifiedOn": "2026-05-07T12:00:00.000Z",
      "owningRoleId": "string",
      "roleDescription": "string",
      "roleId": "string",
      "roleName": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdOn` | date | Creation date. |
| `modifiedOn` | date | Modified date. |
| `owningRoleId` | string | Owning role ID. |
| `roleDescription` | string | Role description. |
| `roleId` | string | Role ID. |
| `roleName` | string | Role name. |

## Native endpoint

Through the native Starburst Galaxy API, this operation is `GET /public/api/v1/role/{roleId}` (base URL `https://mindcloud.galaxy.starburst.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-role.md) for the provider-specific parameters and requirements.

