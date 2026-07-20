# Starburst Galaxy: List roles



```
GET https://connect.mindcloud.co/v1/universal/starburstGalaxy/latest/actions/list-roles
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Starburst Galaxy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/starburstGalaxy/latest/actions/list-roles?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/starburstGalaxy/latest/actions/list-roles?${params}`, {
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

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `pageSize` | number | no | Page size, or 0 for the Starburst Galaxy API default. Current maximum is 100. Example: `100`. |
| `pageToken` | string | no | Pagination token returned by a previous Starburst Galaxy API response. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "nextPageToken": "string",
      "result": [
        {
          "createdOn": "2026-05-07T12:00:00.000Z",
          "modifiedOn": "2026-05-07T12:00:00.000Z",
          "owningRoleId": "string",
          "roleDescription": "string",
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
| `result[].createdOn` | date | Creation date. |
| `result[].modifiedOn` | date | Modified date. |
| `result[].owningRoleId` | string | Owning role ID. |
| `result[].roleDescription` | string | Role description. |
| `result[].roleId` | string | Role ID. |
| `result[].roleName` | string | Role name. |

## Native endpoint

Through the native Starburst Galaxy API, this operation is `GET /public/api/v1/role` (base URL `https://mindcloud.galaxy.starburst.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-roles.md) for the provider-specific parameters and requirements.

