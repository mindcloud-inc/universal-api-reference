# Grist: Get Workspace

Retrieves a workspace from Grist.

```
GET https://connect.mindcloud.co/v1/universal/grist/latest/actions/get-workspace
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Grist `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/grist/latest/actions/get-workspace?connectionId=$CONNECTION_ID&workspaceId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "workspaceId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/grist/latest/actions/get-workspace?${params}`, {
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
| `workspaceId` | list<number> | yes | Workspace ID |

## Response

```json
{
  "success": true,
  "data": [
    {
      "access": "string",
      "createdAt": "string",
      "docs": [
        {
          "access": "string",
          "createdAt": "string",
          "id": "string",
          "isPinned": true,
          "name": "Ava Chen",
          "trunkId": {},
          "type": {},
          "updatedAt": "string",
          "urlId": "https://example.com"
        }
      ],
      "id": 1,
      "isSupportWorkspace": true,
      "name": "Ava Chen",
      "org": {
        "createdAt": "string",
        "domain": "string",
        "host": {},
        "id": 1,
        "name": "Ava Chen",
        "owner": {
          "createdAt": "string",
          "id": 1,
          "name": "Ava Chen",
          "picture": {},
          "ref": "string",
          "type": "string"
        },
        "updatedAt": "string"
      },
      "updatedAt": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `access` | string |  |
| `createdAt` | string |  |
| `docs[].access` | string |  |
| `docs[].createdAt` | string |  |
| `docs[].id` | string |  |
| `docs[].isPinned` | boolean |  |
| `docs[].name` | string |  |
| `docs[].trunkId` | object |  |
| `docs[].type` | object |  |
| `docs[].updatedAt` | string |  |
| `docs[].urlId` | string |  |
| `id` | number |  |
| `isSupportWorkspace` | boolean |  |
| `name` | string |  |
| `org.createdAt` | string |  |
| `org.domain` | string |  |
| `org.host` | object |  |
| `org.id` | number |  |
| `org.name` | string |  |
| `org.owner.createdAt` | string |  |
| `org.owner.id` | number |  |
| `org.owner.name` | string |  |
| `org.owner.picture` | object |  |
| `org.owner.ref` | string |  |
| `org.owner.type` | string |  |
| `org.updatedAt` | string |  |
| `updatedAt` | string |  |

## Native endpoint

Through the native Grist API, this operation is `GET /workspaces/:workspaceId` (base URL `https://docs.getgrist.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-workspace.md) for the provider-specific parameters and requirements.

