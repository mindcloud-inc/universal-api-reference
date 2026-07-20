# Mendix: List User Projects

Retrieves a user's project memberships from Mendix.

```
GET https://connect.mindcloud.co/v1/universal/mendix/latest/actions/list-user-projects
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mendix `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mendix/latest/actions/list-user-projects?connectionId=$CONNECTION_ID&limit=25&offset=0&userId=6f173f40-9e5d-4be0-b698-9ab965c0a31d" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "userId": "6f173f40-9e5d-4be0-b698-9ab965c0a31d"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mendix/latest/actions/list-user-projects?${params}`, {
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
| `userId` | string | yes | The unique identifier of a user. Example: `6f173f40-9e5d-4be0-b698-9ab965c0a31d`. |
| `permissions` | string | no | Comma-separated permissions to filter by, such as administrator, technicalcontact, repositoryaccess, cloudportalaccess, or teamserveraccess. Example: `administrator,repositoryaccess`. |
| `isPinnedByUser` | boolean | no | Whether the user has pinned the project as a favorite. If omitted, both pinned and unpinned projects are returned. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `categories` | string | no | Comma-separated categories with values in the documented Mendix filter format. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "items": [
        {
          "account": {
            "accountId": "string",
            "accountName": "Ava Chen"
          },
          "active": true,
          "description": "string",
          "isPinnedByUser": true,
          "logo": "string",
          "name": "Ava Chen",
          "projectId": "string",
          "role": {
            "hasCloudAccess": true,
            "hasInvitationRights": true,
            "hasRepositoryAccess": true,
            "hasStoryAccess": true,
            "isAdministrator": true,
            "isTechnicalContact": true,
            "name": "Ava Chen"
          },
          "targetCloud": "string"
        }
      ],
      "links": {
        "first": "https://example.com",
        "last": "https://example.com",
        "next": "https://example.com",
        "prev": "https://example.com",
        "self": "https://example.com"
      },
      "page": {
        "elements": 1,
        "offset": 1,
        "totalElements": 1
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `items[].account.accountId` | string | Unique identifier of the account. |
| `items[].account.accountName` | string | Name of the account. |
| `items[].active` | boolean | Indicates whether the project is active. |
| `items[].description` | string | Description of the project. |
| `items[].isPinnedByUser` | boolean | Indicates whether the project was pinned as a favorite. |
| `items[].logo` | string | URL of the project image or logo. |
| `items[].name` | string | Name of the project. |
| `items[].projectId` | string | Unique identifier for the project. |
| `items[].role.hasCloudAccess` | boolean | Indicates whether the user has cloud access. |
| `items[].role.hasInvitationRights` | boolean | Indicates whether the user can invite users to the project team. |
| `items[].role.hasRepositoryAccess` | boolean | Indicates whether the user has repository access. |
| `items[].role.hasStoryAccess` | boolean | Indicates whether the user has story access. |
| `items[].role.isAdministrator` | boolean | Indicates whether the user is a project administrator. |
| `items[].role.isTechnicalContact` | boolean | Indicates whether the user is the technical contact. |
| `items[].role.name` | string | Name of the user's project role. |
| `items[].targetCloud` | string | URL of the cloud portal where the project is hosted. |
| `links.first` | string | First page URL. |
| `links.last` | string | Last page URL. |
| `links.next` | string | Next page URL. |
| `links.prev` | string | Previous page URL. |
| `links.self` | string | Current page URL. |
| `page.elements` | number | Number of elements returned. |
| `page.offset` | number | Pagination offset. |
| `page.totalElements` | number | Total number of matching projects. |

## Native endpoint

Through the native Mendix API, this operation is `GET /users/:userId/projects` (base URL `https://projects-api.home.mendix.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-user-projects.md) for the provider-specific parameters and requirements.

