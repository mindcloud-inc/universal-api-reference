# Timeular: Get Folder

Retrieves a folder from your Timeular workspace.

```
GET https://connect.mindcloud.co/v1/universal/timeular/latest/actions/get-folder
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Timeular `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/timeular/latest/actions/get-folder?connectionId=$CONNECTION_ID&folderId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "folderId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/timeular/latest/actions/get-folder?${params}`, {
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
| `folderId` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "members": [
        {
          "accessLevel": "string",
          "email": "ava@example.com",
          "id": "string",
          "name": "Ava Chen"
        }
      ],
      "name": "Ava Chen",
      "retiredMembers": [
        {
          "id": "string",
          "name": "Ava Chen"
        }
      ],
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |
| `members[].accessLevel` | string |  |
| `members[].email` | string |  |
| `members[].id` | string |  |
| `members[].name` | string |  |
| `name` | string |  |
| `retiredMembers[].id` | string |  |
| `retiredMembers[].name` | string |  |
| `status` | string |  |

## Native endpoint

Through the native Timeular API, this operation is `GET /api/v4/folders/:folderId` (base URL `https://api.early.app`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-folder.md) for the provider-specific parameters and requirements.

