# Documo: Get Folder Info

Retrieves folder details and counts from Documo.

```
GET https://connect.mindcloud.co/v1/universal/documo/latest/actions/get-folder-info
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Documo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/documo/latest/actions/get-folder-info?connectionId=$CONNECTION_ID&folderId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "folderId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/documo/latest/actions/get-folder-info?${params}`, {
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
| `folderId` | string | yes | String \| Required \| Folder UUID |

## Response

```json
{
  "success": true,
  "data": [
    {
      "folder": {
        "accountId": "string",
        "createdAt": "2026-05-07T12:00:00.000Z",
        "hierarchyLevel": 1,
        "id": 1,
        "name": "Ava Chen",
        "parentId": 1,
        "sharedWithAccount": true,
        "updatedAt": "2026-05-07T12:00:00.000Z",
        "uuid": "string"
      },
      "path": [
        {
          "id": 1,
          "name": "Ava Chen",
          "uuid": "string"
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `folder.accountId` | string |  |
| `folder.createdAt` | date |  |
| `folder.hierarchyLevel` | number |  |
| `folder.id` | number |  |
| `folder.name` | string |  |
| `folder.parentId` | number |  |
| `folder.sharedWithAccount` | boolean |  |
| `folder.updatedAt` | date |  |
| `folder.uuid` | string |  |
| `path[].id` | number |  |
| `path[].name` | string |  |
| `path[].uuid` | string |  |

## Native endpoint

Through the native Documo API, this operation is `GET /folders/:folderId/info` (base URL `https://api.documo.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-folder-info.md) for the provider-specific parameters and requirements.

