# Vimeo: Get Project

Retrieves a project record from Vimeo.

```
GET https://connect.mindcloud.co/v1/universal/vimeo/latest/actions/get-project
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Vimeo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/vimeo/latest/actions/get-project?connectionId=$CONNECTION_ID&userId=152184&projectId=12345" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "userId": "152184",
  "projectId": "12345"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/vimeo/latest/actions/get-project?${params}`, {
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
| `userId` | number | yes | The ID of the user. Example: `152184`. |
| `projectId` | number | yes | The ID of the folder. Example: `12345`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accessGrant": {},
      "createdTime": "2026-05-07T12:00:00.000Z",
      "isPinned": true,
      "isPrivateToUser": true,
      "lastUserActionEventDate": "2026-05-07T12:00:00.000Z",
      "link": "https://example.com",
      "manageLink": "https://example.com",
      "metadata": {},
      "modifiedTime": "2026-05-07T12:00:00.000Z",
      "name": "Ava Chen",
      "pinnedOn": "2026-05-07T12:00:00.000Z",
      "privacy": {},
      "resourceKey": "string",
      "uri": "string",
      "user": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accessGrant` | object | The access grant for the project, when present. |
| `createdTime` | date | When the project was created. |
| `isPinned` | boolean | Whether the project is pinned. |
| `isPrivateToUser` | boolean | Whether the project is private to the user. |
| `lastUserActionEventDate` | date | When the last user action occurred in the project. |
| `link` | string | The public project link when Vimeo provides one. |
| `manageLink` | string | The Vimeo manage URL for the project. |
| `metadata` | object | The project metadata connections and interactions. |
| `modifiedTime` | date | When the project was last modified. |
| `name` | string | The project name. |
| `pinnedOn` | date | When the project was pinned, when present. |
| `privacy` | object | The project privacy settings. |
| `resourceKey` | string | The Vimeo resource key for the project. |
| `uri` | string | The project URI. |
| `user` | object | The project owner. |

## Native endpoint

Through the native Vimeo API, this operation is `GET /users/:user_id/projects/:project_id` (base URL `https://api.vimeo.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-project.md) for the provider-specific parameters and requirements.

