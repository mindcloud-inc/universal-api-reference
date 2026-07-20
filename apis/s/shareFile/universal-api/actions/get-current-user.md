# ShareFile: Get Current User



```
GET https://connect.mindcloud.co/v1/universal/shareFile/latest/actions/get-current-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ShareFile `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/shareFile/latest/actions/get-current-user?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/shareFile/latest/actions/get-current-user?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "CanCreateFolders": true,
      "CanManageUsers": true,
      "CanUseFileBox": true,
      "Company": "string",
      "Domain": "string",
      "Email": "ava@example.com",
      "Emails": [
        "ava@example.com"
      ],
      "FirstName": "Ava",
      "FullName": "Ava Chen",
      "Id": "string",
      "IsAdministrator": true,
      "LastName": "Chen",
      "odata": {
        "metadata": "string",
        "type": "string"
      },
      "Roles": [
        "string"
      ],
      "url": "https://example.com",
      "Username": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `CanCreateFolders` | boolean | Whether the returned user can create folders. |
| `CanManageUsers` | boolean | Whether the returned user can manage users. |
| `CanUseFileBox` | boolean | Whether the returned user can use File Box. |
| `Company` | string | The ShareFile company name. |
| `Domain` | string | The ShareFile domain. |
| `Email` | string | The primary email address. |
| `Emails` | array<string> | The user email addresses. |
| `FirstName` | string | The user first name. |
| `FullName` | string | The user full name. |
| `Id` | string | The ShareFile user identifier. |
| `IsAdministrator` | boolean | Whether the returned user is an administrator. |
| `LastName` | string | The user last name. |
| `odata.metadata` | string | The OData metadata URL for the returned user. |
| `odata.type` | string | The OData type for the returned user. |
| `Roles` | array<string> | The user roles. |
| `url` | string | The API URL for the returned user resource. |
| `Username` | string | The ShareFile username. |

## Native endpoint

Through the native ShareFile API, this operation is `GET /Users` (base URL `https://{{credentials.accessTokenRequest.subdomain}}.{{credentials.accessTokenRequest.apicp}}/sf/v3`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/get-current-user.md) for the provider-specific parameters and requirements.

