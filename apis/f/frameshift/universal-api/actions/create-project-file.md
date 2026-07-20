# Frameshift: Create Project File

Creates a project file in Frameshift.

```
POST https://connect.mindcloud.co/v1/universal/frameshift/latest/actions/create-project-file
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Frameshift `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/frameshift/latest/actions/create-project-file" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "projectId": "string",
  "uri": "string",
  "name": "Ava Chen",
  "reference": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/frameshift/latest/actions/create-project-file', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "projectId": "string",
    "uri": "string",
    "name": "Ava Chen",
    "reference": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `projectId` | string | yes | Resource identifier for the project to access |
| `uri` | string | yes | The resource location of the file |
| `name` | string | yes | The name of the file |
| `reference` | string | yes | The genome build of the file |
| `type` | string | no | The file type of the file |

## Response

```json
{
  "success": true,
  "data": [
    {
      "bedFileId": {},
      "createdAt": "string",
      "gcpBucketId": {},
      "id": 1,
      "libraryType": {},
      "md5Checksum": {},
      "name": "Ava Chen",
      "nickname": "Ava Chen",
      "projectId": 1,
      "reference": "string",
      "s3BucketId": {},
      "sampleId": {},
      "size": {},
      "type": "string",
      "updatedAt": "string",
      "uri": "string",
      "vcfSampleName": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `bedFileId` | object |  |
| `createdAt` | string |  |
| `gcpBucketId` | object |  |
| `id` | number |  |
| `libraryType` | object |  |
| `md5Checksum` | object |  |
| `name` | string |  |
| `nickname` | string |  |
| `projectId` | number |  |
| `reference` | string |  |
| `s3BucketId` | object |  |
| `sampleId` | object |  |
| `size` | object |  |
| `type` | string |  |
| `updatedAt` | string |  |
| `uri` | string |  |
| `vcfSampleName` | object |  |

## Native endpoint

Through the native Frameshift API, this operation is `POST /v1/projects/:project_id/files` (base URL `https://mosaic.frameshift.io/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-project-file.md) for the provider-specific parameters and requirements.

