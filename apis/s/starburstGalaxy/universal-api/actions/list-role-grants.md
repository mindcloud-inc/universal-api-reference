# Starburst Galaxy: List role grants



```
GET https://connect.mindcloud.co/v1/universal/starburstGalaxy/latest/actions/list-role-grants
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Starburst Galaxy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/starburstGalaxy/latest/actions/list-role-grants?connectionId=$CONNECTION_ID&roleId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "roleId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/starburstGalaxy/latest/actions/list-role-grants?${params}`, {
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
| `roleId` | string | yes | Starburst Galaxy role ID. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `pageSize` | number | no | Page size, or 0 for the Starburst Galaxy API default. Current maximum is 100. Example: `100`. |
| `pageToken` | string | no | Pagination token returned by a previous Starburst Galaxy API response. |
| `type` | string | no | Optional role grant type filter documented by the Starburst Galaxy API. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "nextPageToken": "string",
      "result": [
        {
          "adminOption": true,
          "principal": {},
          "roleId": "string",
          "roleName": "Ava Chen"
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `nextPageToken` | string | The next page token to use or empty string if there are no more pages. |
| `result[].adminOption` | boolean | Whether admin option is enabled. |
| `result[].principal` | object | Granted principal. |
| `result[].roleId` | string | Role ID. |
| `result[].roleName` | string | Role name. |

## Native endpoint

Through the native Starburst Galaxy API, this operation is `GET /public/api/v1/role/{roleId}/rolegrant` (base URL `https://mindcloud.galaxy.starburst.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-role-grants.md) for the provider-specific parameters and requirements.

