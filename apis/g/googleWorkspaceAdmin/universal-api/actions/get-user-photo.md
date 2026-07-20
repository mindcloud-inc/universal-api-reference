# Google Workspace Admin: Get User Photo

Retrieves a user's photo from Google Workspace Admin.

```
GET https://connect.mindcloud.co/v1/universal/googleWorkspaceAdmin/latest/actions/get-user-photo
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Google Workspace Admin `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/googleWorkspaceAdmin/latest/actions/get-user-photo?connectionId=$CONNECTION_ID&userKey=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "userKey": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/googleWorkspaceAdmin/latest/actions/get-user-photo?${params}`, {
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
      "etag": "string",
      "height": 1,
      "id": "string",
      "kind": "string",
      "mimeType": "string",
      "photoData": "string",
      "primaryEmail": "ava@example.com",
      "width": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `etag` | string |  |
| `height` | number |  |
| `id` | string |  |
| `kind` | string |  |
| `mimeType` | string |  |
| `photoData` | string |  |
| `primaryEmail` | string |  |
| `width` | number |  |

## Native endpoint

Through the native Google Workspace Admin API, this operation is `GET /admin/directory/v1/users/:userKey/photos/thumbnail` (base URL `https://admin.googleapis.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-user-photo.md) for the provider-specific parameters and requirements.

