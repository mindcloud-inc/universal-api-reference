# GitBook: List Organization Members

Retrieves members from a GitBook organization.

```
GET https://connect.mindcloud.co/v1/universal/gitBook/latest/actions/list-organization-members
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GitBook `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/gitBook/latest/actions/list-organization-members?connectionId=$CONNECTION_ID&limit=25&offset=0&organizationId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "organizationId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/gitBook/latest/actions/list-organization-members?${params}`, {
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
| `role` | string | no |  |
| `search` | string | no |  |
| `sort` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "disabled": true,
      "id": "string",
      "joinedAt": "2026-05-07T12:00:00.000Z",
      "lastSeenAt": "2026-05-07T12:00:00.000Z",
      "object": "string",
      "role": "string",
      "spaces": 1,
      "sso": true,
      "teams": 1,
      "user": {
        "displayName": "Ava Chen",
        "email": "ava@example.com",
        "id": "string",
        "photoURL": "https://example.com",
        "urls": {
          "location": "https://example.com"
        }
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `disabled` | boolean |  |
| `id` | string |  |
| `joinedAt` | date |  |
| `lastSeenAt` | date |  |
| `object` | string |  |
| `role` | string |  |
| `spaces` | number |  |
| `sso` | boolean |  |
| `teams` | number |  |
| `user.displayName` | string |  |
| `user.email` | string |  |
| `user.id` | string |  |
| `user.photoURL` | string |  |
| `user.urls.location` | string |  |

## Native endpoint

Through the native GitBook API, this operation is `GET /orgs/:organizationId/members` (base URL `https://api.gitbook.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-organization-members.md) for the provider-specific parameters and requirements.

