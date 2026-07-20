# Frameshift: List Project Files

Retrieves a list of project files from Frameshift.

```
GET https://connect.mindcloud.co/v1/universal/frameshift/latest/actions/list-project-files
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Frameshift `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/frameshift/latest/actions/list-project-files?connectionId=$CONNECTION_ID&limit=25&offset=0&projectId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "projectId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/frameshift/latest/actions/list-project-files?${params}`, {
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
| `projectId` | string | yes | Resource identifier for the project to access |
| `search` | string | no | The search keyword to filter the results by |

## Response

```json
{
  "success": true,
  "data": [
    {
      "count": 1,
      "data": [
        {
          "bedFileId": {},
          "createdAt": "string",
          "endpointUrl": {},
          "gcpBucketId": {},
          "gcpBucketName": {},
          "gcpEndpointUrl": {},
          "id": 1,
          "libraryType": {},
          "md5Checksum": {},
          "name": "Ava Chen",
          "nickname": "Ava Chen",
          "projectId": 1,
          "reference": "string",
          "s3BucketId": {},
          "s3BucketName": {},
          "sampleId": {},
          "size": {},
          "type": "string",
          "updatedAt": "string",
          "uri": "string",
          "vcfSampleName": {}
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
| `count` | number |  |
| `data[].bedFileId` | object |  |
| `data[].createdAt` | string |  |
| `data[].endpointUrl` | object |  |
| `data[].gcpBucketId` | object |  |
| `data[].gcpBucketName` | object |  |
| `data[].gcpEndpointUrl` | object |  |
| `data[].id` | number |  |
| `data[].libraryType` | object |  |
| `data[].md5Checksum` | object |  |
| `data[].name` | string |  |
| `data[].nickname` | string |  |
| `data[].projectId` | number |  |
| `data[].reference` | string |  |
| `data[].s3BucketId` | object |  |
| `data[].s3BucketName` | object |  |
| `data[].sampleId` | object |  |
| `data[].size` | object |  |
| `data[].type` | string |  |
| `data[].updatedAt` | string |  |
| `data[].uri` | string |  |
| `data[].vcfSampleName` | object |  |

## Native endpoint

Through the native Frameshift API, this operation is `GET /v1/projects/:project_id/files` (base URL `https://mosaic.frameshift.io/api`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-project-files.md) for the provider-specific parameters and requirements.

