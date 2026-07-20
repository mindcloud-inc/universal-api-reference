# Seqera: Describe Workspace

Retrieves workspace details from Seqera.

```
GET https://connect.mindcloud.co/v1/universal/seqera/latest/actions/describe-workspace
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Seqera `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/seqera/latest/actions/describe-workspace?connectionId=$CONNECTION_ID&orgId=1&workspaceId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "orgId": "1",
  "workspaceId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/seqera/latest/actions/describe-workspace?${params}`, {
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
| `workspaceId` | number | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "workspace": {
        "dateCreated": "2026-05-07T12:00:00.000Z",
        "description": "string",
        "fullName": "Ava Chen",
        "id": 1,
        "lastUpdated": "2026-05-07T12:00:00.000Z",
        "name": "Ava Chen",
        "visibility": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `workspace` | object | Workspace details. |
| `workspace.dateCreated` | date | Workspace creation timestamp. |
| `workspace.description` | string | Workspace description. |
| `workspace.fullName` | string | Full workspace name. |
| `workspace.id` | number | Workspace ID. |
| `workspace.lastUpdated` | date | Workspace update timestamp. |
| `workspace.name` | string | Workspace name. |
| `workspace.visibility` | string | Workspace visibility. |

## Native endpoint

Through the native Seqera API, this operation is `GET /orgs/:orgId/workspaces/:workspaceId` (base URL `https://api.cloud.seqera.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/describe-workspace.md) for the provider-specific parameters and requirements.

