# Zoho Projects: List Portal Users, Client Users, And Contacts

Retrieves portal users, client users, and contacts from Zoho Projects.

```
GET https://connect.mindcloud.co/v1/universal/zohoProjects/latest/actions/list-portal-users-client-users-and-contacts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Projects `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zohoProjects/latest/actions/list-portal-users-client-users-and-contacts?connectionId=$CONNECTION_ID&limit=25&offset=0&portalId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "portalId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zohoProjects/latest/actions/list-portal-users-client-users-and-contacts?${params}`, {
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
| `portalId` | string | yes | Zoho Projects portal ID. |
| `type` | number | no | User type selector. |
| `viewType` | string | no | User activity view type. |
| `sort` | string | no | Sort order. |
| `ids` | string | no | Comma-separated user IDs. |
| `companyIds` | string | no | Comma-separated customer IDs. |
| `view` | string | no | Data view type. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `filter` | string | no | Raw JSON filter object from Zoho Projects. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "pageInfo": {
        "count": 1,
        "hasNextPage": true,
        "page": 1,
        "perPage": 1
      },
      "users": [
        [
          {}
        ]
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `pageInfo.count` | number |  |
| `pageInfo.hasNextPage` | boolean |  |
| `pageInfo.page` | number |  |
| `pageInfo.perPage` | number |  |
| `users[]` | array<object> |  |
| `users[].addedTime` | date |  |
| `users[].associatedServices[]` | array<string> |  |
| `users[].budget` | string |  |
| `users[].businessHours.id` | string |  |
| `users[].businessHours.name` | string |  |
| `users[].businessHours.version` | number |  |
| `users[].businessHours.workingHours[]` | array<object> |  |
| `users[].displayName` | string |  |
| `users[].email` | string |  |
| `users[].firstName` | string |  |
| `users[].fullName` | string |  |
| `users[].id` | string |  |
| `users[].isActive` | boolean |  |
| `users[].isConfirmed` | boolean |  |
| `users[].lastAccessedOn` | date |  |
| `users[].lastName` | string |  |
| `users[].profile.id` | string |  |
| `users[].profile.isDefault` | boolean |  |
| `users[].profile.name` | string |  |
| `users[].profile.type` | string |  |
| `users[].role.id` | string |  |
| `users[].role.name` | string |  |
| `users[].role.type` | string |  |
| `users[].status` | string |  |
| `users[].timeOfRequest` | string |  |
| `users[].updatedTime` | date |  |
| `users[].userType` | string |  |
| `users[].zuid` | number |  |

## Native endpoint

Through the native Zoho Projects API, this operation is `GET /portal/[:PORTALID]/users` (base URL `https://projectsapi.zoho.com/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-portal-users-client-users-and-contacts.md) for the provider-specific parameters and requirements.

