# Google Workspace Admin: List User Aliases

Retrieves a user's aliases from Google Workspace Admin.

```
GET https://connect.mindcloud.co/v1/universal/googleWorkspaceAdmin/latest/actions/list-user-aliases
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Google Workspace Admin `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/googleWorkspaceAdmin/latest/actions/list-user-aliases?connectionId=$CONNECTION_ID&userKey=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "userKey": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/googleWorkspaceAdmin/latest/actions/list-user-aliases?${params}`, {
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
| `userKey` | string | yes | User primary email, alias, or unique ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "aliases": [
        {
          "alias": "string",
          "etag": "string",
          "id": "string",
          "kind": "string",
          "primaryEmail": "ava@example.com"
        }
      ],
      "etag": "string",
      "kind": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `aliases[].alias` | string |  |
| `aliases[].etag` | string |  |
| `aliases[].id` | string |  |
| `aliases[].kind` | string |  |
| `aliases[].primaryEmail` | string |  |
| `etag` | string |  |
| `kind` | string |  |

## Native endpoint

Through the native Google Workspace Admin API, this operation is `GET /admin/directory/v1/users/:userKey/aliases` (base URL `https://admin.googleapis.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-user-aliases.md) for the provider-specific parameters and requirements.

