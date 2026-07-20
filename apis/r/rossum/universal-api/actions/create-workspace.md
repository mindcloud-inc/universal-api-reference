# Rossum: Create Workspace

Creates a new workspace in Rossum.

```
POST https://connect.mindcloud.co/v1/universal/rossum/latest/actions/create-workspace
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rossum `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/rossum/latest/actions/create-workspace" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen",
  "organization": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/rossum/latest/actions/create-workspace', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen",
    "organization": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | Name of the workspace to create. |
| `organization` | string | yes | Organization URL that owns the workspace. |
| `autopilot` | boolean | no | Whether autopilot should be enabled for the workspace. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "autopilot": true,
      "id": 1,
      "modifiedAt": "string",
      "modifiedBy": "string",
      "name": "Ava Chen",
      "organization": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `autopilot` | boolean |  |
| `id` | number |  |
| `modifiedAt` | string |  |
| `modifiedBy` | string |  |
| `name` | string |  |
| `organization` | string |  |
| `url` | string |  |

## Native endpoint

Through the native Rossum API, this operation is `POST /workspaces` (base URL `https://mindcloud.rossum.app/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-workspace.md) for the provider-specific parameters and requirements.

