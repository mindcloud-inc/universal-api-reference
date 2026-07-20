# Seqera: List Organization Workspaces

Retrieves organization workspaces from Seqera.

```
GET https://connect.mindcloud.co/v1/universal/seqera/latest/actions/list-organization-workspaces
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Seqera `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/seqera/latest/actions/list-organization-workspaces?connectionId=$CONNECTION_ID&orgId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "orgId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/seqera/latest/actions/list-organization-workspaces?${params}`, {
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
| `orgId` | number | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "workspaces": [
        {
          "description": "string",
          "fullName": "Ava Chen",
          "id": 1,
          "name": "Ava Chen",
          "visibility": "string"
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
| `workspaces` | array<object> | Organization workspaces. |
| `workspaces[].description` | string | Workspace description. |
| `workspaces[].fullName` | string | Full workspace name. |
| `workspaces[].id` | number | Workspace ID. |
| `workspaces[].name` | string | Workspace name. |
| `workspaces[].visibility` | string | Workspace visibility. |

## Native endpoint

Through the native Seqera API, this operation is `GET /orgs/:orgId/workspaces` (base URL `https://api.cloud.seqera.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-organization-workspaces.md) for the provider-specific parameters and requirements.

