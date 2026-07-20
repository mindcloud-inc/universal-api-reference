# Timeular: Get Folder Member

Retrieves a folder member from your Timeular workspace.

```
GET https://connect.mindcloud.co/v1/universal/timeular/latest/actions/get-folder-member
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Timeular `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/timeular/latest/actions/get-folder-member?connectionId=$CONNECTION_ID&folderId=string&memberId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "folderId": "string",
  "memberId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/timeular/latest/actions/get-folder-member?${params}`, {
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
| `memberId` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accessLevel": "string",
      "email": "ava@example.com",
      "id": "string",
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accessLevel` | string |  |
| `email` | string |  |
| `id` | string |  |
| `name` | string |  |

## Native endpoint

Through the native Timeular API, this operation is `GET /api/v4/folders/:folderId/members/:memberId` (base URL `https://api.early.app`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-folder-member.md) for the provider-specific parameters and requirements.

