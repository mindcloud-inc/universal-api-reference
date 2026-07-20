# Socket: List Repositories

Retrieves organization repositories available in Socket.

```
GET https://connect.mindcloud.co/v1/universal/socket/latest/actions/list-repositories
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Socket `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/socket/latest/actions/list-repositories?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/socket/latest/actions/list-repositories?${params}`, {
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
| `direction` | string | no |  |
| `includeArchived` | boolean | no |  |
| `page` | number | no |  |
| `perPage` | number | no |  |
| `sort` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "nextPage": 1,
      "results": [
        {
          "archived": true,
          "createdAt": "string",
          "defaultBranch": "string",
          "description": "string",
          "headFullScanId": "string",
          "homepage": "string",
          "id": "string",
          "integrationMeta": {
            "type": "string",
            "value": {}
          },
          "name": "Ava Chen",
          "slug": "string",
          "updatedAt": "string",
          "visibility": "string",
          "workspace": "string"
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
| `nextPage` | number |  |
| `results` | array<object> |  |
| `results[]` | object |  |
| `results[].archived` | boolean | Whether the repository is archived or not |
| `results[].createdAt` | string | The creation date of the repository |
| `results[].defaultBranch` | string | The default branch of the repository |
| `results[].description` | string | The description of the repository |
| `results[].headFullScanId` | string | The ID of the head full scan of the repository |
| `results[].homepage` | string | The homepage URL of the repository |
| `results[].id` | string | The ID of the repository |
| `results[].integrationMeta` | object |  |
| `results[].integrationMeta.type` | string |  |
| `results[].integrationMeta.value` | object |  |
| `results[].name` | string | The name of the repository |
| `results[].slug` | string | The slug of the repository |
| `results[].updatedAt` | string | The last update date of the repository |
| `results[].visibility` | string | The visibility of the repository |
| `results[].workspace` | string | The workspace of the repository |

## Native endpoint

Through the native Socket API, this operation is `GET /orgs/:org_slug/repos` (base URL `https://api.socket.dev/v0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-repositories.md) for the provider-specific parameters and requirements.

