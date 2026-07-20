# Blaze AI: List Docs

Retrieves documents from a Blaze AI workspace.

```
GET https://connect.mindcloud.co/v1/universal/blazeAI/latest/actions/list-docs
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Blaze AI `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/blazeAI/latest/actions/list-docs?connectionId=$CONNECTION_ID&limit=25&offset=0&workspace_id=994619" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "workspace_id": "994619"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/blazeAI/latest/actions/list-docs?${params}`, {
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
| `workspace_id` | number | yes | Blaze workspace ID. Default: `994619`. |
| `folderId` | number | no | Optional folder filter. Default: `3413829`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        {
          "createdAt": "string",
          "folderId": 1,
          "id": 1,
          "key": "string",
          "ownerId": 1,
          "title": "string",
          "updatedAt": "string",
          "workspaceId": 1
        }
      ],
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data[].createdAt` | string |  |
| `data[].folderId` | number |  |
| `data[].id` | number |  |
| `data[].key` | string |  |
| `data[].ownerId` | number |  |
| `data[].title` | string |  |
| `data[].updatedAt` | string |  |
| `data[].workspaceId` | number |  |
| `success` | boolean |  |

## Native endpoint

Through the native Blaze AI API, this operation is `GET /api/v1/w/:workspace_id/docs` (base URL `https://api.blaze.ai`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-docs.md) for the provider-specific parameters and requirements.

