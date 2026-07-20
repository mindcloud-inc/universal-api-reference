# GitBook: List Spaces

Retrieves spaces from a GitBook organization.

```
GET https://connect.mindcloud.co/v1/universal/gitBook/latest/actions/list-spaces
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GitBook `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/gitBook/latest/actions/list-spaces?connectionId=$CONNECTION_ID&limit=25&offset=0&organizationId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "organizationId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/gitBook/latest/actions/list-spaces?${params}`, {
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
| `organizationId` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "changeRequests": 1,
      "changeRequestsDraft": 1,
      "changeRequestsOpen": 1,
      "comments": 1,
      "createdAt": "2026-05-07T12:00:00.000Z",
      "defaultLevel": "string",
      "editMode": "string",
      "emoji": "string",
      "id": "string",
      "mergeRules": {
        "type": "string"
      },
      "object": "string",
      "organization": "string",
      "permissions": {
        "access": true,
        "admin": true,
        "comment": true,
        "edit": true,
        "installIntegration": true,
        "merge": true,
        "review": true,
        "triggerGitSync": true,
        "view": true,
        "viewInviteLinks": true
      },
      "revision": "string",
      "title": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "urls": {
        "app": "https://example.com",
        "location": "https://example.com"
      },
      "visibility": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `changeRequests` | number |  |
| `changeRequestsDraft` | number |  |
| `changeRequestsOpen` | number |  |
| `comments` | number |  |
| `createdAt` | date |  |
| `defaultLevel` | string |  |
| `editMode` | string |  |
| `emoji` | string |  |
| `id` | string |  |
| `mergeRules.type` | string |  |
| `object` | string |  |
| `organization` | string |  |
| `permissions.access` | boolean |  |
| `permissions.admin` | boolean |  |
| `permissions.comment` | boolean |  |
| `permissions.edit` | boolean |  |
| `permissions.installIntegration` | boolean |  |
| `permissions.merge` | boolean |  |
| `permissions.review` | boolean |  |
| `permissions.triggerGitSync` | boolean |  |
| `permissions.view` | boolean |  |
| `permissions.viewInviteLinks` | boolean |  |
| `revision` | string |  |
| `title` | string |  |
| `updatedAt` | date |  |
| `urls.app` | string |  |
| `urls.location` | string |  |
| `visibility` | string |  |

## Native endpoint

Through the native GitBook API, this operation is `GET /orgs/:organizationId/spaces` (base URL `https://api.gitbook.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-spaces.md) for the provider-specific parameters and requirements.

