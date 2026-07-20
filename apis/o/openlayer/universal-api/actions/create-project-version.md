# Openlayer: Create Project Version

Creates a new project version in Openlayer.

```
POST https://connect.mindcloud.co/v1/universal/openlayer/latest/actions/create-project-version
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Openlayer `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/openlayer/latest/actions/create-project-version" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "commit.message": "MindCloud version seed",
  "commit.source": "api",
  "projectId": "2fcd0a42-23a7-44bb-b4fa-4fc3168fe248",
  "storageUri": "s3://api-openlayer-assets-us-west-2/workspaces/b9ef2789-e1dd-4946-9ab0-189dcee20750/users/5e0d836f-f7a3-45db-bb5a-632f9e03aa8d/uploads/1775742330-d2efa942/mindcloud-openlayer-runtime.bin"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/openlayer/latest/actions/create-project-version', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "commit.message": "MindCloud version seed",
    "commit.source": "api",
    "projectId": "2fcd0a42-23a7-44bb-b4fa-4fc3168fe248",
    "storageUri": "s3://api-openlayer-assets-us-west-2/workspaces/b9ef2789-e1dd-4946-9ab0-189dcee20750/users/5e0d836f-f7a3-45db-bb5a-632f9e03aa8d/uploads/1775742330-d2efa942/mindcloud-openlayer-runtime.bin"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `commit.message` | string | yes | Commit message. Default: `MindCloud version seed`. |
| `commit.source` | string | yes | Commit source. Default: `api`. |
| `projectId` | string | yes | The Openlayer project ID. Default: `2fcd0a42-23a7-44bb-b4fa-4fc3168fe248`. |
| `runtime` | string | no | Execution runtime. Default: `python_3_11`. |
| `storageUri` | string | yes | Uploaded artifact storage URI. Default: `s3://api-openlayer-assets-us-west-2/workspaces/b9ef2789-e1dd-4946-9ab0-189dcee20750/users/5e0d836f-f7a3-45db-bb5a-632f9e03aa8d/uploads/1775742330-d2efa942/mindcloud-openlayer-runtime.bin`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "commit": {
        "id": "string",
        "message": "string",
        "source": "string"
      },
      "dateCreated": "string",
      "deploymentStatus": "string",
      "id": "string",
      "links": {
        "app": "https://example.com"
      },
      "projectId": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `commit.id` | string |  |
| `commit.message` | string |  |
| `commit.source` | string |  |
| `dateCreated` | string |  |
| `deploymentStatus` | string |  |
| `id` | string |  |
| `links.app` | string |  |
| `projectId` | string |  |
| `status` | string |  |

## Native endpoint

Through the native Openlayer API, this operation is `POST /projects/:projectId/versions` (base URL `https://api.openlayer.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-project-version.md) for the provider-specific parameters and requirements.

