# Mendix: List Account Projects

Retrieves company-owned projects for an account in Mendix.

```
GET https://connect.mindcloud.co/v1/universal/mendix/latest/actions/list-account-projects
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mendix `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mendix/latest/actions/list-account-projects?connectionId=$CONNECTION_ID&limit=25&offset=0&accountId=b8f3f8f9-245e-4c9e-b0a1-69d2e1f2aa10" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "accountId": "b8f3f8f9-245e-4c9e-b0a1-69d2e1f2aa10"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mendix/latest/actions/list-account-projects?${params}`, {
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
| `accountId` | string | yes | The unique identifier of the account or company. Example: `b8f3f8f9-245e-4c9e-b0a1-69d2e1f2aa10`. |
| `createdSince` | date | no | Only return projects created after this UTC date and time, such as 2020-01-16T05:53:28Z. Example: `2020-01-16T05:53:28Z`. |

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
          "active": true,
          "createdBy": {
            "fullName": "Ava Chen",
            "userId": "string"
          },
          "createdOn": "string",
          "description": "string",
          "logo": "string",
          "name": "Ava Chen",
          "projectId": "string"
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
| `items[].active` | boolean | Indicates whether the project is active. |
| `items[].createdBy.fullName` | string | Full name of the user who created the project. |
| `items[].createdBy.userId` | string | Unique identifier of the user who created the project. |
| `items[].createdOn` | string | Date and time when the project was created. |
| `items[].description` | string | Description of the project. |
| `items[].logo` | string | URL of the project image or logo. |
| `items[].name` | string | Name of the project. |
| `items[].projectId` | string | Unique identifier for the project. |
| `links.first` | string | First page URL. |
| `links.last` | string | Last page URL. |
| `links.next` | string | Next page URL. |
| `links.prev` | string | Previous page URL. |
| `links.self` | string | Current page URL. |
| `page.elements` | number | Number of elements returned. |
| `page.offset` | number | Pagination offset. |
| `page.totalElements` | number | Total number of matching projects. |

## Native endpoint

Through the native Mendix API, this operation is `GET /accounts/:accountId/projects` (base URL `https://projects-api.home.mendix.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-account-projects.md) for the provider-specific parameters and requirements.

