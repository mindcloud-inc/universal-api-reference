# ManyReach: Create Workspace

Creates a new workspace in ManyReach.

```
POST https://connect.mindcloud.co/v1/universal/manyReach/latest/actions/create-workspace
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ManyReach `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/manyReach/latest/actions/create-workspace" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "title": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/manyReach/latest/actions/create-workspace', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "title": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `title` | string | yes | Workspace title. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "apiKey": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "title": "string",
      "workspaceId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `apiKey` | string | API key for authenticating requests made on behalf of this workspace, represented as a GUID. |
| `createdAt` | date | Timestamp when the workspace was created in the system. |
| `title` | string | Display name of the workspace; maximum 256 characters. |
| `workspaceId` | number | Unique identifier for the workspace (sub-organization) within the agency. |

## Native endpoint

Through the native ManyReach API, this operation is `POST https://api.manyreach.com/api/v2/workspaces` (base URL `https://api.manyreach.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-workspace.md) for the provider-specific parameters and requirements.

