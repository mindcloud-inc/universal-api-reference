# Grist: List Workspaces

Finds workspaces in a Grist organization.

```
GET https://connect.mindcloud.co/v1/universal/grist/latest/actions/list-workspaces
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Grist `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/grist/latest/actions/list-workspaces?connectionId=$CONNECTION_ID&orgId=current" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "orgId": "current"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/grist/latest/actions/list-workspaces?${params}`, {
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
| `orgId` | list<number> | yes | Organization ID or current Default: `current`. |

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
          "public": true,
          "trunkId": {},
          "type": {},
          "updatedAt": "string",
          "urlId": "https://example.com"
        }
      ],
      "id": 1,
      "isSupportWorkspace": true,
      "name": "Ava Chen",
      "orgDomain": "string",
      "owner": {
        "anonymous": true,
        "createdAt": "string",
        "email": "ava@example.com",
        "id": 1,
        "name": "Ava Chen",
        "options": {
          "locale": "string"
        },
        "picture": {},
        "ref": "string",
        "type": "string"
      },
      "public": true,
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
| `docs[].public` | boolean |  |
| `docs[].trunkId` | object |  |
| `docs[].type` | object |  |
| `docs[].updatedAt` | string |  |
| `docs[].urlId` | string |  |
| `id` | number |  |
| `isSupportWorkspace` | boolean |  |
| `name` | string |  |
| `orgDomain` | string |  |
| `owner.anonymous` | boolean |  |
| `owner.createdAt` | string |  |
| `owner.email` | string |  |
| `owner.id` | number |  |
| `owner.name` | string |  |
| `owner.options.locale` | string |  |
| `owner.picture` | object |  |
| `owner.ref` | string |  |
| `owner.type` | string |  |
| `public` | boolean |  |
| `updatedAt` | string |  |

## Native endpoint

Through the native Grist API, this operation is `GET /orgs/:orgId/workspaces` (base URL `https://docs.getgrist.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-workspaces.md) for the provider-specific parameters and requirements.

