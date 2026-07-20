# Frameshift: Create Sample File

Creates a sample file in Frameshift.

```
POST https://connect.mindcloud.co/v1/universal/frameshift/latest/actions/create-sample-file
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Frameshift `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/frameshift/latest/actions/create-sample-file" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "projectId": "string",
  "sampleId": "string",
  "uri": "string",
  "name": "Ava Chen",
  "reference": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/frameshift/latest/actions/create-sample-file', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "projectId": "string",
    "sampleId": "string",
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
| `sampleId` | string | yes | Resource identifier for the sample to access |
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
      "created_at": "2026-05-07T12:00:00.000Z",
      "id": 1,
      "name": "Ava Chen",
      "nickname": "Ava Chen",
      "reference": "string",
      "sample_id": 1,
      "type": "string",
      "updated_at": "2026-05-07T12:00:00.000Z",
      "uri": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created_at` | date |  |
| `id` | number |  |
| `name` | string |  |
| `nickname` | string |  |
| `reference` | string |  |
| `sample_id` | number |  |
| `type` | string |  |
| `updated_at` | date |  |
| `uri` | string |  |

## Native endpoint

Through the native Frameshift API, this operation is `POST /v1/projects/:project_id/samples/:sample_id/files` (base URL `https://mosaic.frameshift.io/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-sample-file.md) for the provider-specific parameters and requirements.

